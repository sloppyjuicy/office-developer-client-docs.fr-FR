---
title: CommandType, propriété (ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472554"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="f7784-102">CommandType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f7784-102">CommandType Property (ADO)</span></span>


<span data-ttu-id="f7784-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7784-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7784-104">Indique le type d'un objet [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f7784-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f7784-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f7784-105">Settings and Return Values</span></span>

<span data-ttu-id="f7784-106">Définit ou renvoie une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="f7784-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f7784-p101">[!REMARQUE] N'utilisez pas les valeurs <STRONG>CommandTypeEnum</STRONG> <STRONG>adCmdFile</STRONG> ou <STRONG>adCmdTableDirect</STRONG> avec la propriété <STRONG>CommandType</STRONG>. Ces valeurs peuvent être uniquement utilisées en tant qu'options avec les méthodes <A href="open-method-ado-recordset.md">Open</A> et <A href="requery-method-ado.md">Requery</A> d'un objet <A href="recordset-object-ado.md">Recordset</A>.</span><span class="sxs-lookup"><span data-stu-id="f7784-p101">Do not use the <STRONG>CommandTypeEnum</STRONG> values of <STRONG>adCmdFile</STRONG> or <STRONG>adCmdTableDirect</STRONG> with <STRONG>CommandType</STRONG>. These values can only be used as options with the <A href="open-method-ado-recordset.md">Open</A> and <A href="requery-method-ado.md">Requery</A> methods of a <A href="recordset-object-ado.md">Recordset</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="f7784-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f7784-109">Remarks</span></span>

<span data-ttu-id="f7784-110">Utilisez la propriété **CommandType** pour optimiser l'évaluation de la propriété [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f7784-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="f7784-p102">Si la valeur de la propriété **CommandType** est égale à **adCmdUnknown** (valeur par défaut), vous pouvez connaître une dégradation des performances car ADO doit effectuer des appels auprès du fournisseur pour déterminer si la propriété **CommandText** est une instruction SQL, une procédure stockée ou le nom d'une table. Si vous connaissez le type de commande utilisé, la définition de la propriété **CommandType** permet à ADO d'accéder directement au code approprié. Si la propriété **CommandType** ne correspond pas au type de commande dans la propriété **CommandText**, une erreur se produit lorsque vous appelez la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f7784-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

