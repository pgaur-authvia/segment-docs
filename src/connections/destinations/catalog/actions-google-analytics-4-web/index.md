---
title: Google Analytics 4 Web Destination
strat: google
hide-boilerplate: true
hide-dossier: false
id: 63ed446fe60a1b56c5e6f130
versions:
  - name: "Google Analytics 4 Cloud"
    link: '/docs/connections/destinations/catalog/actions-google-analytics-4/'
---

{% include content/plan-grid.md name="actions" %}

[Google Analytics 4](https://support.google.com/analytics/answer/10089681){:target="_blank"} is Google's new Analytics property, which you can use for both websites and applications. Google Analytics 4 has machine learning at its core to help surface insights and give you a more complete understanding of your customers across devices and platforms. 

When you have Segment installed, you can use your existing tracking implementation to fulfill your data collection needs with Google Analytics 4. When you use the Google Analytics 4 Web destination, Segment loads the [gtag.js library](https://support.google.com/analytics/answer/9310895?hl=en#zippy=%2Cin-this-article){:target="_blank"}  for you. 

> info ""
> The Google Analytics 4 Web destination is in beta and is in active development. Some functionality may change before it becomes generally available.

## Getting started

Before you connect Segment to Google Analytics 4, configure a Google Analytics 4 property in your Analytics account. For more information, see Google's article [Set up Analytics for a website and/or app](https://support.google.com/analytics/answer/9304153){:target='_blank'}.

To connect the Google Analytics 4 Web destination: 

1. From the Segment web app, click **Catalog**, then click **Destinations**.
2. Search for “Google Analytics 4 Web” in the Destinations Catalog, and select the destination.
3. Click **Configure Google Analytics 4 Web**.
4. Select the web source that will send data to Google Analytics 4 and follow the steps to name your destination. The web source chosen must use [Analytics.js 2.0](/docs/connections/sources/catalog/libraries/website/javascript/){:target='_blank'}.
5. On the **Settings** tab, under **Basic Settings**, enter in the [Measurement ID](https://support.google.com/analytics/answer/9539598){:target='_blank'} associated with your GA4 web stream.
6. Follow the steps in the Destinations Actions documentation on [Customizing mappings](/docs/connections/destinations/actions/#customizing-mappings).

{% include components/actions-fields.html settings="true"%}

## FAQ & Troubleshooting

### Custom Event Naming

Google Analytics 4 does not accept custom event names that include spaces. Segment replaces spaces in the Event Name in the Custom Event action with an underscore. As a result, you will see custom events snake cased in Google Analytics 4.

Google Analytics 4 is also case sensitive. If you would like all event names to be lowercase, use the `Lowercase Event Name` setting in the Custom Event action. If this setting is disabled, Google will treat event names with different casing as distinct events. For more information, see [Google Analytics 4 Event name rules](https://support.google.com/analytics/answer/10085872?hl=en&ref_topic=9756175#event-name-rules&zippy=%2Cin-this-article.%2Cin-this-article){:target="_blank"}.

### Custom Dimensions & Metrics

With Google Analytics 4, you must create custom dimensions and metrics within the Google Analytics 4 interface and link event parameters to the corresponding dimension or metric. When creating the dimension or metric, you can either select a parameter from the list of already collected fields or enter the name of the parameter you plan to collect in the future. For more information, see [Google Analytics 4 Custom dimensions and metrics](https://support.google.com/analytics/answer/10075209?hl=en){:target="_blank"}.

### Debug Mode

The Google Analytics 4 [debug mode](https://support.google.com/analytics/answer/7201382?hl=en){:target="_blank"} is supported with the Google Analytics 4 Web destination. DebugView displays the events and user properties that Analytics collects from a user in real-time. This can be helpful in troubleshooting your implementation.