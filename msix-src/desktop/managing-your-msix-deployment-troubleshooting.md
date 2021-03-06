---
Description: This article provides all the details you need to manage deploying you MSIX applications in an enterprise environment.  This article is targeted at enterprise and IT Pros.
title: Managing your MSIX deployment
ms.date: 2/3/2020
ms.topic: article
keywords: windows 10, deployment, msix
ms.assetid:  
ms.localizationpriority: medium
---

# MSIX Validation and Troubleshooting
Though MSIX has a 99% successful install rate, sometimes you need to be able to trouble shoot an installation.

## Know the application
Understanding the application that you are installing and how it works can go a long way to troubleshooting the user experience.  For example, does the application have certain limitations that could be causing the issues?  Does the user have access to the resources needed by the application?  Were there dependencies the application had, that were not met by the current operating system?

## Test your application
Before deploying your application, make sure you have tested your application.  The Windows SDK provides a tool, the Windows App Certification kit that can identify common issues before publication.  
To install the latest Windows SDK, [go here.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
To learn more about the Windows App Certification Kit, see [Windows App Certification Kit](https://docs.microsoft.com/windows/uwp/debug-test-perf/windows-app-certification-kit)

## Flight your application
Another great way to catch issues early is to flight your applications.  If you are deploying through the Windows store or Microsoft Store for Business, you can use package flights to deploy your application to a subset of individuals to get additional real world testing.  
To learn more about flighting, see [Package flighting.](https://docs.microsoft.com/windows/uwp/publish/package-flights?context=/windows/msix/render)

## Device Portal and Debugging
Sometimes it is necessary to interact with the application in the user's environment to adequately understand the issue.  Windows provides a powerful tool, the [Device Portal Desktop](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal-desktop) which will allow you to connect to the device and interact with the application remotely.  
To learn more about Device Portal, see [Device Portal Desktop.](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal-desktop)
To learn more about Debugging MSIX packages, see [Run, debug, and test a packaged desktop application.](https://docs.microsoft.com/windows/msix/desktop/desktop-to-uwp-debug)

## Installation issues
When there are issues with the installation, you can investigate the artifacts provided by AppInstaller.  First, AppInstaller provides error code failures.  If the error code for any failure is not sufficient to determine what is wrong, the AppInstaller also logs all interactions to the Event Viewer.  You will find the logs here: Application and Services Logs->Microsoft->Windows->AppxDeployment-Server.

You can use the Event Viewer or Powershell to access those events. 
To learn more about how to view the events, see [Troubleshooting packaging, deployment, and query of Windows apps.](https://docs.microsoft.com/windows/win32/appxpkg/troubleshooting)

To learn more about AppInstaller troubleshooting, see [Troubleshoot Appinstaller Issues.](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues)


## Next steps

Have questions? Ask us on Stack Overflow. Our team monitors these [tags](https://stackoverflow.com/questions/tagged/project-centennial+or+desktop-bridge). You can also ask us [here](https://social.msdn.microsoft.com/Forums//home?filter=alltypes&sort=relevancedesc&searchTerm=%5BDesktop%20Converter%5D).

 
