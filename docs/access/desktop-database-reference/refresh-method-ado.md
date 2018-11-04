---
title: Refresh, méthode (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d7548a31518f225c15dbf0e9a6de2b82c66c72af
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950138"
---
# <a name="refresh-method-ado"></a>Refresh, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Met à jour les objets d'une collection pour qu'ils reflètent les objets disponibles ou spécifiques au fournisseur.

## <a name="syntax"></a>Syntaxe

la *collection*. Actualiser

## <a name="remarks"></a>Notes

La méthode **Refresh** exécute différentes tâches selon la collection à partir de laquelle vous l'appelez.

## <a name="parameters"></a>Collection Parameters

Lorsque vous appliquez la méthode **Refresh** à la collection [Parameters](command-object-ado.md) d'un objet [Command](parameters-collection-ado.md), des informations de paramètres côté fournisseur sont extraites pour la procédure stockée ou la requête paramétrée spécifiée dans l'objet **Command**. La collection est vide pour les fournisseurs qui ne prennent pas en charge les appels de procédure stockée et les requêtes paramétrées.

Affectez un objet [Connection](activeconnection-property-ado.md) valide à la propriété **ActiveConnection** de l'objet [Command](connection-object-ado.md), une commande valide à la propriété [CommandText](commandtext-property-ado.md) et la valeur [adCmdStoredProc](commandtype-property-ado.md) à la propriété **CommandType** avant d'appeler la méthode **Refresh**.

Si vous accédez à la collection **Parameters** avant d'appeler la méthode **Refresh**, ADO appelle automatiquement cette méthode et remplit la collection.

> [!NOTE]
> [!REMARQUE] Si vous utilisez la méthode **Refresh** pour obtenir des paramètres du fournisseur et que cette méthode retourne un ou plusieurs objets [Parameter](parameter-object-ado.md) qui possèdent un type de données de longueur variable, ADO peut allouer de la mémoire à ces paramètres en fonction de leur taille maximale potentielle, ce qui entraîne une erreur lors de l'exécution. Pour éviter ces erreurs, vous devez définir explicitement la propriété [Size](size-property-ado.md) de ces paramètres avant d'appeler la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

### <a name="fields"></a>Fields

L'application de la méthode **Refresh** à la collection **Fields** ne produit aucun effet visible. Pour extraire des modifications de la structure de base de données sous-jacente , vous devez utiliser la méthode [Requery](requery-method-ado.md) ou, si l'objet [Recordset](recordset-object-ado.md) ne prend pas en charge les signets, la méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

### <a name="properties"></a>Propriétés

L'application de la méthode **Refresh** à la collection **Properties** de certains objets remplit cette collection de propriétés dynamiques exposées par le fournisseur. Ces propriétés fournissent des informations sur les fonctionnalités propres au fournisseur, au-delà des propriétés intégrées prises en charge par ADO.

