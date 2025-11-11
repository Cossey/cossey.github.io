---
title: openHAB
---
openHAB is an open source smart home platform, built primarily in Java, that brings together devices, services, and technologies from different vendors into a single, flexible system.

I’ve been using openHAB for over five years and actively contributing to its ecosystem. One of the key extension points in openHAB is its “bindings.” A binding is an add-on that integrates a specific device, service, or protocol into openHAB, exposing it as things and channels so it can be automated and controlled just like any other part of your smart home.

Below are some of the bindings and contributions I’ve worked on.

## HP Printer Binding

I originally created this binding to monitor and integrate my HP OfficeJet printer with openHAB.

Many HP printers expose status and metrics through their built-in web interface as XML. The binding connects to that interface and reads those XML files to retrieve useful information, such as:

- Ink levels
- Event and page counts
- Printer and scanner status

The community played a big part in shaping this binding by testing with different printer models and sharing their XML outputs. That input helped broaden compatibility and improve reliability.

## Hamilton City Council Rubbish Collection Binding

This binding was built to solve a real-world problem: rubbish and recycling reminders that stay accurate.

While collection normally follows a weekly schedule with alternating bins, public holidays can shift collection days. Instead of relying on guesswork, this binding:

- Fetches current collection information
- Accounts for schedule changes
- Feeds accurate dates into openHAB

From there, it can be used to send reminders or trigger notifications so people know exactly which bins to put out and when.

## NZ Water Alerts Binding

This binding provides water restriction alerts for various regions in New Zealand.

Different alert levels come with rules around water usage, and not following them can lead to fines and unnecessary waste. Integrated into openHAB, this information can:

- Control or pause irrigation automations
- Help households stay compliant with restrictions
- Support more responsible water use

This binding is one of the more challenging ones to maintain. There are no official APIs, so it relies on scraping council and provider websites and processing the results. When those sites change layout or structure, the binding needs updates to keep working correctly.

## Other Contributions

Alongside these bindings, I’ve also made smaller contributions across the openHAB project, including:

- Improvements to the Onkyo binding
- Enhancements and refinements to Main UI

openHAB has a strong community and a powerful architecture, and contributing to it has been a rewarding way to combine my interest in automation, reliability, and real-world problem solving.
