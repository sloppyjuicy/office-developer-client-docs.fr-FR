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
ms.localizationpriority: medium
ms.openlocfilehash: c8dd0d49a1bf544e967c36b3a9ba8c368e002b10
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365963"
---
# <a name="commandtype-property-ado"></a>CommandType, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le type d'un objet [Command](command-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md).

> [!NOTE]
> [!REMARQUE] N'utilisez pas les valeurs **CommandTypeEnum** **adCmdFile** ou **adCmdTableDirect** avec la propriété **CommandType**. Ces valeurs peuvent être uniquement utilisées en tant qu'options avec les méthodes [Open](open-method-ado-recordset.md) et [Requery](requery-method-ado.md) d'un objet [Recordset](recordset-object-ado.md).


## <a name="remarks"></a>Remarques

Utilisez la propriété **CommandType** pour optimiser l'évaluation de la propriété [CommandText](commandtext-property-ado.md).

Si la valeur de la propriété **CommandType** est égale à **adCmdUnknown** (valeur par défaut), vous pouvez connaître une dégradation des performances car ADO doit effectuer des appels auprès du fournisseur pour déterminer si la propriété **CommandText** est une instruction SQL, une procédure stockée ou le nom d'une table. Si vous connaissez le type de commande utilisé, la définition de la propriété **CommandType** permet à ADO d'accéder directement au code approprié. Si la propriété **CommandType** ne correspond pas au type de commande dans la propriété **CommandText**, une erreur se produit lorsque vous appelez la méthode [Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

