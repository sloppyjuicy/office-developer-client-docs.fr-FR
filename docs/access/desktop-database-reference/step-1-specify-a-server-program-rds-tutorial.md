---
title: 'Étape 1 : spécifier un programme serveur (didacticiel RDS)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89aa87aa63a3d8bfdeb291f78d6525f51c4262b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469057"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="07245-102">Étape 1 : spécifier un programme serveur (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="07245-102">Step 1: Specify a Server Program (RDS Tutorial)</span></span>


<span data-ttu-id="07245-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07245-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07245-p101">Dans la plupart des cas, utilisez la méthode [CreateObject](createobject-method-rds.md) de l’objet [RDS.DataSpace](dataspace-object-rds.md) pour spécifier le programme serveur par défaut, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou votre propre programme serveur personnalisé (objet métier). Un programme serveur est instancié sur le serveur et une référence à ce programme (ou *proxy*) est retournée.</span><span class="sxs-lookup"><span data-stu-id="07245-p101">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="07245-106">Ce didacticiel utilise le programme serveur par défaut :</span><span class="sxs-lookup"><span data-stu-id="07245-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

