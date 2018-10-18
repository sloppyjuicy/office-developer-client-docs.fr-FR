---
title: 'Étape 5 : mise à disposition de DataControl (didacticiel RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d5b0dfef4d14594c2b2a9b8b57b866e032a07a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605652"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="11200-102">Étape 5 : mise à disposition de DataControl (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="11200-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="11200-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="11200-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="11200-p101">L'objet **Recordset** retourné est disponible et peut être utilisé. Vous pouvez l'examiner, le parcourir ou le modifier comme n'importe quel autre objet **Recordset**. L'utilisation que vous pouvez faire de cet objet **Recordset** dépend de votre environnement. Visual Basic et Visual C++ intègrent des contrôles visuels qu'un objet **Recordset** peut utiliser directement ou indirectement à l'aide d'un contrôle d'activation de données.</span><span class="sxs-lookup"><span data-stu-id="11200-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="11200-108"><<<<<<< Tête par exemple, si vous affichez une page Web dans Microsoft Internet Explorer, vous souhaitez afficher les données de l’objet **Recordset** dans un contrôle visuel.</span><span class="sxs-lookup"><span data-stu-id="11200-108"><<<<<<< HEAD For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="11200-109">Les contrôles visuels d’une page Web ne peut pas accéder à un objet **Recordset** directement.</span><span class="sxs-lookup"><span data-stu-id="11200-109">Visual controls on a Web page cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="11200-110">Cependant, ils peuvent accéder à l’objet **Recordset** par le biais de la [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="11200-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="11200-111">**RDS. DataControl** utilisable par un contrôle visuel lorsque sa propriété [SourceRecordset](recordset-sourcerecordset-properties-rds.md) est définie à l’objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="11200-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>
<span data-ttu-id="11200-112">=== Par exemple, si vous affichez une page Web dans Microsoft Internet Explorer, vous souhaitez afficher les données de l’objet **Recordset** dans un contrôle visuel.</span><span class="sxs-lookup"><span data-stu-id="11200-112">======= For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="11200-113">Les contrôles visuels d’une page Web ne peut pas accéder à un objet **Recordset** directement.</span><span class="sxs-lookup"><span data-stu-id="11200-113">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="11200-114">Cependant, ils peuvent accéder à l’objet **Recordset** par le biais de la [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="11200-114">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="11200-115">**RDS. DataControl** utilisable par un contrôle visuel lorsque sa propriété [SourceRecordset](recordset-sourcerecordset-properties-rds.md) est définie à l’objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="11200-115">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>
>>>>>>> <span data-ttu-id="11200-116">master</span><span class="sxs-lookup"><span data-stu-id="11200-116">master</span></span>

<span data-ttu-id="11200-117">Le paramètre **DATASRC** de l'objet de contrôle visuel doit être défini sur **RDS.DataControl**, et sa propriété **DATAFLD** sur un champ (colonne) de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="11200-117">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="11200-118">Dans ce didacticiel, définissez la propriété **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="11200-118">In this tutorial, set the **SourceRecordset** property:</span></span>

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

