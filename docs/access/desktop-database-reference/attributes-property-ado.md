---
title: Attributes, propriété (ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0edebe425b025e3b3497640a7e436b5996493dae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558883"
---
# <a name="attributes-property-ado"></a>Attributes, propriété (ADO)


**S’applique à** : Access 2013, Office 2013


## <a name="attributes-property"></a>Attributes, propriété

Indique une ou plusieurs caractéristiques d'un objet.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long**.

Pour un objet [Connection](connection-object-ado.md), la propriété **Attributes** est en lecture/écriture et sa valeur peut être la somme d'une ou de plusieurs valeurs de [XactAttributeEnum](xactattributeenum.md). La valeur par défaut est zéro (0).

Pour un objet [Parameter](parameter-object-ado.md), la propriété **Attributes** est en lecture/écriture et sa valeur peut être la somme d'une ou de plusieurs valeurs de [ParameterAttributesEnum](parameterattributesenum.md). La valeur par défaut est **adParamSigned**.

Pour un objet [Field](field-object-ado.md), la propriété **Attributes** peut être la somme d'une ou de plusieurs valeurs de [FieldAttributeEnum](fieldattributeenum.md). Elle est normalement en lecture seule. Cependant, pour les nouveaux objets **Field** qui ont été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Attributes** est en lecture/écriture uniquement après que la propriété [Value](value-property-ado.md) de l'objet **Field** a été spécifiée et que le nouvel objet **Field** a pu être ajouté par le fournisseur de données par un appel de la méthode [Update](update-method-ado.md) de la collection **Fields**.

Pour un objet [Property](property-object-ado.md), la propriété **Attributes** est en lecture seule et sa valeur peut être la somme d’une ou plusieurs valeurs de [PropertyAttributesEnum](propertyattributesenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Attributes** pour définir ou retourner les caractéristiques des objets **Connection**, **Parameter**, [Field](field-object-ado.md) ou [Property](property-object-ado.md).

Lorsque vous définissez plusieurs attributs, vous pouvez additionner les constantes appropriées. Si vous attribuez à la propriété une valeur représentant une somme qui inclut des constantes incompatibles, une erreur est générée.

**Utilisation du service de données à distance** Cette propriété n’est pas disponible sur un objet **Connection** côté client.

