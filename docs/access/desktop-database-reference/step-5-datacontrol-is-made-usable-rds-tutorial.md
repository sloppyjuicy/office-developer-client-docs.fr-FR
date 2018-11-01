---
title: 'Étape 5 : mise à disposition de DataControl (didacticiel RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5871138f2b82770f49da2d5f9d4977443b0664e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884043"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="9a4c0-102">Étape 5 : DataControl est disponible (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="9a4c0-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="9a4c0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a4c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a4c0-p101">L'objet **Recordset** retourné est disponible et peut être utilisé. Vous pouvez l'examiner, le parcourir ou le modifier comme n'importe quel autre objet **Recordset**. L'utilisation que vous pouvez faire de cet objet **Recordset** dépend de votre environnement. Visual Basic et Visual C++ intègrent des contrôles visuels qu'un objet **Recordset** peut utiliser directement ou indirectement à l'aide d'un contrôle d'activation de données.</span><span class="sxs-lookup"><span data-stu-id="9a4c0-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="9a4c0-108">Par exemple, si vous affichez une page Web dans Microsoft Internet Explorer, vous souhaitez afficher les données de l’objet **Recordset** dans un contrôle visuel.</span><span class="sxs-lookup"><span data-stu-id="9a4c0-108">For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="9a4c0-109">Les contrôles visuels d’une page Web ne peut pas accéder à un objet **Recordset** directement.</span><span class="sxs-lookup"><span data-stu-id="9a4c0-109">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="9a4c0-110">Cependant, ils peuvent accéder à l’objet **Recordset** par le biais de la [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9a4c0-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="9a4c0-111">**RDS. DataControl** utilisable par un contrôle visuel lorsque sa propriété [SourceRecordset](recordset-sourcerecordset-properties-rds.md) est définie à l’objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9a4c0-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="9a4c0-112">Le paramètre **DATASRC** de l'objet de contrôle visuel doit être défini sur **RDS.DataControl**, et sa propriété **DATAFLD** sur un champ (colonne) de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9a4c0-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="9a4c0-113">Dans ce didacticiel, définissez la propriété **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="9a4c0-113">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

