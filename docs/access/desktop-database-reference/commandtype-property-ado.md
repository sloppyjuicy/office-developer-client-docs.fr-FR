---
title: CommandType, propriété (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880235"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="98128-102">CommandType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="98128-102">CommandType property (ADO)</span></span>


<span data-ttu-id="98128-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98128-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98128-104">Indique le type d'un objet [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="98128-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="98128-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="98128-105">Settings and return values</span></span>

<span data-ttu-id="98128-106">Définit ou renvoie une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="98128-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="98128-p101">[!REMARQUE] N'utilisez pas les valeurs **CommandTypeEnum** **adCmdFile** ou **adCmdTableDirect** avec la propriété **CommandType**. Ces valeurs peuvent être uniquement utilisées en tant qu'options avec les méthodes [Open](open-method-ado-recordset.md) et [Requery](requery-method-ado.md) d'un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="98128-p101">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**. These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="98128-109">Notes</span><span class="sxs-lookup"><span data-stu-id="98128-109">Remarks</span></span>

<span data-ttu-id="98128-110">Utilisez la propriété **CommandType** pour optimiser l'évaluation de la propriété [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="98128-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="98128-p102">Si la valeur de la propriété **CommandType** est égale à **adCmdUnknown** (valeur par défaut), vous pouvez connaître une dégradation des performances car ADO doit effectuer des appels auprès du fournisseur pour déterminer si la propriété **CommandText** est une instruction SQL, une procédure stockée ou le nom d'une table. Si vous connaissez le type de commande utilisé, la définition de la propriété **CommandType** permet à ADO d'accéder directement au code approprié. Si la propriété **CommandType** ne correspond pas au type de commande dans la propriété **CommandText**, une erreur se produit lorsque vous appelez la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).</span><span class="sxs-lookup"><span data-stu-id="98128-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

