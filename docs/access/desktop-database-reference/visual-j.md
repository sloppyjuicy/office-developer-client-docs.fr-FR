---
title: Visual J++ (référence de base de données de bureau Access)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da13ae0f10e2338b961f2f12686bd378580a69d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311332"
---
# <a name="visual-j"></a><span data-ttu-id="c4b4e-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="c4b4e-102">Visual J++</span></span>


<span data-ttu-id="c4b4e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4b4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4b4e-104">Ce petit exemple Microsoft Visual J++ illustre comment associer votre propre fonction à un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="c4b4e-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

```java 
 
// BeginEventExampleVJ 
import com.ms.wfc.data.*; 
 
public class EventExampleVJ 
{ 
 ConnectionEventHandler handler = new ConnectionEventHandler(this,"onConnectComplete"); 
 
 public void onConnectComplete(Object sender,ConnectionEvent e) 
 { 
 if (e.adStatus == AdoEnums.EventStatus.ERRORSOCCURRED) 
 System.out.println("Connection failed"); 
 else 
 System.out.println("Connection completed"); 
 return; 
 } 
 
 public static void main (String[] args) 
 { 
 EventExampleVJ Class1 = new EventExampleVJ(); 
 Connection conn = new Connection(); 
 
 conn.addOnConnectComplete(Class1.handler); // Enable event support. 
 conn.open("DSN=Pubs"); 
 conn.close(); 
 conn.removeOnConnectComplete(Class1.handler); // Disable event support. 
 } 
} 
// EndEventExampleVJ 
```

<span data-ttu-id="c4b4e-105">Tout d'abord, la méthode de classe *onConnectionComplete* est associée à l'événement **ConnectionComplete** en créant un nouvel objet **ConnectionEventHandler** et en y assignant la fonction *onConnectComplete*.</span><span class="sxs-lookup"><span data-stu-id="c4b4e-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="c4b4e-106">La fonction *main* crée un objet **Connection** et active la gestion des événements en invoquant la méthode **addOnConnectComplete** et en lui transmettant l'adresse de la fonction *handler*.</span><span class="sxs-lookup"><span data-stu-id="c4b4e-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

