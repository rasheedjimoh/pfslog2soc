# Ingesting pfSense Logs into Security Onion

## Introduction

Welcome to my professional portfolio, where I demonstrate expertise in cybersecurity infrastructure setup. Today, I'll guide you through the process of integrating pfSense logs into Security Onion using Elastic Fleet, enhancing network security monitoring and threat detection capabilities.

## Why We Need It

Incorporating pfSense logs into Security Onion is essential for bolstering network security monitoring and threat detection capabilities. Here's why this integration is crucial:

1. **Enhanced Threat Visibility:**
   - Integrating pfSense logs into Security Onion provides comprehensive visibility into network activities and security events. By aggregating and analysing pfSense logs alongside other network data, Security Onion enables security teams to detect and respond to potential threats more effectively.

2. **Proactive Threat Detection:**
   - Security Onion's advanced analytics capabilities allow for proactive threat detection by correlating pfSense logs with other security events. This enables security teams to identify suspicious behaviour and potential security incidents before they escalate, mitigating risks and minimizing the impact on the organization.

3. **Streamlined Incident Response:**
   - By centralizing pfSense logs within Security Onion, organizations can streamline incident response processes. Security Onion's intuitive interface and automation features facilitate rapid investigation and response to security incidents, enabling security teams to mitigate threats promptly and minimize downtime.

4. **Compliance and Reporting:**
   - Integrating pfSense logs into Security Onion helps organizations meet compliance requirements by providing comprehensive log data for auditing and reporting purposes. Security Onion's robust reporting capabilities enable organizations to demonstrate compliance with regulatory standards and industry best practices, enhancing trust and credibility with stakeholders.

In summary, integrating pfSense logs into Security Onion is essential for enhancing network security monitoring, threat detection, and incident response capabilities. By aggregating and analysing pfSense logs within Security Onion, organizations can proactively identify and mitigate security threats, thereby safeguarding their network infrastructure and sensitive data.

---

## Ingesting pfSense Logs into Security Onion

1. **Login to Elastic Fleet:**
   - Access Elastic Fleet and add the Elastic integration to the General Policy to manage agent policies efficiently.
![pf-ingest](https://github.com/rasheedjimoh/pfslog2soc/assets/157264080/cd06b30e-e3a9-4125-8dcc-3c2f2126a99a)



2. **Configure Integration for pfSense:**
   - Within the Agent policies, add the pfSense integration and set the syslog host to "0.0.0.0.0" to ensure Security Onion captures all management traffic on UDP port 9001.

3. **Save and Deploy Changes:**
   - Save the configuration changes and deploy them to ensure seamless integration between pfSense and Security Onion.

**Configuring Security Onion:**

1. **Adjusting Firewall Settings:**
   - Access the Security Onion host administration panel and navigate to the Configuration section to configure firewall settings.
   - Enable "show all configurable settings" and configure custom host and port groups to accommodate pfSense log traffic on UDP port 9001.

![pf-ingest0](https://github.com/rasheedjimoh/pfslog2soc/assets/157264080/44fef836-76cd-4425-a932-6d5392906544)


2. **Defining Role and License:**
   - Set the role to Standalone and configure the chain and input settings to accept traffic from the custom port group assigned to pfSense logs.

3. **Synchronizing Changes:**
   - Push the configuration changes into production by synchronizing the grid, ensuring seamless integration and data flow between pfSense and Security Onion.

![pf-ingest1](https://github.com/rasheedjimoh/pfslog2soc/assets/157264080/223062c9-a94b-4e14-ab1b-6cb608cc0f9b)

## Configuring pfSense

1. **Enabling Remote Logging:**
   - Configure pfSense to send logs by enabling remote logging in the system logs settings.
   - Specify the LAN as the source address and set the remote log server to the Security Onion IP address and port 9001, ensuring comprehensive log forwarding.

2. **Sending All Logs:**
   - Configure pfSense to send all logs to Security Onion for thorough network monitoring and threat detection.

By following these steps, you can effectively integrate pfSense logs into Security Onion, enhancing your network security posture and enabling proactive threat detection and response.



## Conclusion

In conclusion, integrating pfSense logs into Security Onion is a crucial step towards strengthening network security and enhancing threat detection capabilities. By following the outlined steps to configure this integration, organizations can effectively centralize and analyze pfSense logs within Security Onion, enabling proactive threat detection and efficient incident response.

Stay vigilant, stay secure!
