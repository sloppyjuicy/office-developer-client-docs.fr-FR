---
title: "Étape 4 : le serveur retourne l'objet Recordset (didacticiel RDS)"
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 515573d9992ec85652897ff08b034bee02beea9d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946159"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a><span data-ttu-id="c65ff-102">Étape 4 : Le serveur retourne l’objet Recordset (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="c65ff-102">Step 4: Server returns the Recordset (RDS Tutorial)</span></span>

<span data-ttu-id="c65ff-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c65ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c65ff-p101">RDS convertit l'objet **Recordset** récupéré dans un format qui peut être renvoyé au client (autrement dit, il *marshale* l'objet **Recordset**). La forme exacte de la conversion et son mode d'envoi varient selon que le serveur réside sur Internet ou sur un intranet, sur un réseau local ou qu'il corresponde à une bibliothèque de liaison dynamique. Toutefois, ce détail n'est pas crucial ; l'important est que RDS renvoie l'objet **Recordset** au client.</span><span class="sxs-lookup"><span data-stu-id="c65ff-p101">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**). The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="c65ff-107">Côté client, un objet **Recordset** est retourné et affecté à une variable locale.</span><span class="sxs-lookup"><span data-stu-id="c65ff-107">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

