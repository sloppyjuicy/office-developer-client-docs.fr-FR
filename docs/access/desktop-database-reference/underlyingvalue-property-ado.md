---
title: UnderlyingValue, propriété (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313999"
---
# <a name="underlyingvalue-property-ado"></a>UnderlyingValue, propriété (ADO)


**S’applique à** : Access 2013, Office 2013



Indique la valeur actuelle d'un objet [Field](field-object-ado.md) dans la base de données.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **Variant** qui indique la valeur de l'objet **Field**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **UnderlyingValue** pour renvoyer la valeur actuelle du champ de la base de données. La valeur du champ dans la propriété **UnderlyingValue** est celle qui est visible pour votre transaction et peut résulter d'une mise à jour récente effectuée par une autre transaction. Elle peut être différente de la propriété [OriginalValue](originalvalue-property-ado.md), qui reflète la valeur renvoyée à l'origine à l'objet [Recordset](recordset-object-ado.md).

Cette procédure est similaire à la méthode [Resync](resync-method-ado.md), mais la propriété **UnderlyingValue** renvoie uniquement la valeur d'un champ spécifique de l'enregistrement actuel. C'est cette valeur que la méthode [Resync](resync-method-ado.md) utilise pour remplacer la propriété [Value](value-property-ado.md).

Lorsque vous utilisez cette propriété en association avec la propriété **OriginalValue**, vous pouvez résoudre les conflits générés par les mises à jour par lot.

## <a name="record"></a>Record

Pour les objets [Record](record-object-ado.md), cette propriété est vide pour les champs ajoutés avant l’appel de la méthode [Update](update-method-ado.md).

