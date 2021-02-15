---
title: Resync, méthode (ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fa483d86dc345968607a0752f0552ddccfe7fef5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306572"
---
# <a name="resync-method-ado"></a>Resync, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Cette méthode actualise les données de l’objet [Recordset](recordset-object-ado.md) actif ou la collection [Fields](fields-collection-ado.md) d’un objet [Record](record-object-ado.md) à partir de la base de données sous-jacente.

## <a name="syntax"></a>Syntaxe

*Recordset*. Resync *AffectRecords*, *ResyncValues*

*Enregistrement*. *Champs*. Resync *ResyncValues*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*AffectRecords* |Facultatif. La valeur [AffectEnum](affectenum.md) détermine combien d'enregistrements sont affectés par la méthode **Resync**. La valeur **adAffectAll** est utilisée par défaut ; elles n'est pas disponible avec la méthode **Resync** de la collection **Fields** d'un objet **Record**.|
|*ResyncValues* |Facultatif. La valeur [ResyncEnum](resyncenum.md) indique si les valeurs sous-jacentes sont remplacées. La valeur par défaut est **adResyncAllValues**.|

## <a name="remarks"></a>Remarques

### <a name="recordset"></a>Recordset

Faites appel à la méthode **Resync** pour resynchroniser des enregistrements de l'objet **Recordset** actif sur la base de données sous-jacente. Ceci est utile si vous utilisez un curseur statique ou avant uniquement, mais que vous voulez afficher les modifications apportées dans la base de données sous-jacente.

Si vous affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, **Resync** n'est disponible que pour les objets **Recordset** en lecture-écriture.

Contrairement à la méthode [Requery](requery-method-ado.md), la méthode **Resync** ne réexécute pas la commande sous-jacente de l'objet **Recordset**. Les nouveaux enregistrements de la base de données sous-jacente ne seront pas visibles.

Si la tentative de resynchronisation échoue à cause d’un conflit avec les données sous-jacentes (par exemple, un enregistrement a été supprimé par un autre utilisateur), le fournisseur retourne des avertissements à la collection [Errors](errors-collection-ado.md) et une erreur d’exécution se produit. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) et [Status](status-property-ado-recordset.md) pour identifier les enregistrements qui créent des conflits.

Si les propriétés dynamiques [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et [Resync Command](resync-command-property-dynamic-ado.md) sont définies et que l'objet **Recordset** obtenu provient de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Resync** exécute la commande fournie dans la propriété **Resync Command** uniquement au niveau de la table désignée dans la propriété **Unique Table**.

### <a name="fields"></a>Champs

Faites appel à la méthode **Resync** pour resynchroniser les valeurs de la collection **Fields** d’un objet **Record** sur la source de données sous-jacente. La propriété [Count](count-property-ado.md) n’est pas affectée par cette méthode.

Si *ResyncValues* a la valeur par défaut **adResyncAllValues**, les propriétés [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md) et [OriginalValue](originalvalue-property-ado.md) des objets [Field](field-object-ado.md) de la collection sont synchronisés. Si *ResyncValues* a la valeur **adResyncUnderlyingValues**, seule la propriété **UnderlyingValue** est synchronisée.

The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**. For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect. For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.

**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.

