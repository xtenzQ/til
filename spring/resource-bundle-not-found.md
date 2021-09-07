# Resource Bundle not found

In case of getting:
> WARNING: ResourceBundle [resourcebundles/messages] not found for MessageSource: Can't find bundle for base name resources/messages, locale en_US
Exception in thread "main" org.springframework.context.NoSuchMessageException: No message found under code 'user.welcome' for locale 'en_US'.

In your `*-servlet.xml` instead of using `ResourceBundleMessageSource` try `ReloadableResourceBundleMessageSource` like this:
```XML
<bean id="messageSource" class="org.springframework.context.support.ResourceBundleMessageSource">
    <property name="basename" value="classpath:messages" />
</bean>

<hr>

[Return](../../../)
```