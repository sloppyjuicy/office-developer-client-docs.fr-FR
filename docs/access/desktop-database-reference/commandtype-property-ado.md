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
# <a name="commandtype-property-ado"></a>CommandType, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le type d'un objet [Command](command-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md).


> [!NOTE]
> <P>[!REMARQUE] N'utilisez pas les valeurs <STRONG>CommandTypeEnum</STRONG> <STRONG>adCmdFile</STRONG> ou <STRONG>adCmdTableDirect</STRONG> avec la propriété <STRONG>CommandType</STRONG>. Ces valeurs peuvent être uniquement utilisées en tant qu'options avec les méthodes <A href="open-method-ado-recordset.md">Open</A> et <A href="requery-method-ado.md">Requery</A> d'un objet <A href="recordset-object-ado.md">Recordset</A>.</P>



## <a name="remarks"></a>Notes

Utilisez la propriété **CommandType** pour optimiser l'évaluation de la propriété [CommandText](commandtext-property-ado.md).

Si la valeur de la propriété **CommandType** est égale à **adCmdUnknown** (valeur par défaut), vous pouvez connaître une dégradation des performances car ADO doit effectuer des appels auprès du fournisseur pour déterminer si la propriété **CommandText** est une instruction SQL, une procédure stockée ou le nom d'une table. Si vous connaissez le type de commande utilisé, la définition de la propriété **CommandType** permet à ADO d'accéder directement au code approprié. Si la propriété **CommandType** ne correspond pas au type de commande dans la propriété **CommandText**, une erreur se produit lorsque vous appelez la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).

