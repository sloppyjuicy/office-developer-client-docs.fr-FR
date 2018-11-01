---
title: DefinedSize, propriété (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868853"
---
# <a name="definedsize-property-ado"></a>DefinedSize, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique la capacité en données d'un objet [Field](field-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** qui reflète la taille définie pour un champ sous la forme d'un nombre d'octets.

## <a name="remarks"></a>Notes

Utilisez la propriété **DefinedSize** pour déterminer la capacité en données d'un objet **Field**.

Les propriétés **DefinedSize** et [ActualSize](actualsize-property-ado.md) sont différentes. Par exemple, imaginez un objet **Field** avec le type déclaré **adVarChar** et une propriété **DefinedSize** de 50, contenant un caractère unique. La valeur retournée pour la propriété **ActualSize** correspond à la longueur en octets du caractère unique.

