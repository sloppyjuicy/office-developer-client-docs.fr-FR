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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709872"
---
# <a name="resync-method-ado"></a>Resync, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Cette méthode actualise les données de l'objet [Recordset](recordset-object-ado.md) actif ou la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md) à partir de la base de données sous-jacente.

## <a name="syntax"></a>Syntaxe

*Jeu d’enregistrements*. Resync*AffectRecords*, *ResyncValues*

*Enregistrement*. *Champs*. Resync*ResyncValues*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*AffectRecords* |Facultatif. La valeur [AffectEnum](affectenum.md) détermine combien d'enregistrements sont affectés par la méthode **Resync**. La valeur **adAffectAll** est utilisée par défaut ; elles n'est pas disponible avec la méthode **Resync** de la collection **Fields** d'un objet **Record**.|
|*ResyncValues* |Facultatif. La valeur [ResyncEnum](resyncenum.md) indique si les valeurs sous-jacentes sont remplacées. La valeur par défaut est **adResyncAllValues**.|

## <a name="remarks"></a>Notes

### <a name="recordset"></a>Recordset

Faites appel à la méthode **Resync** pour resynchroniser des enregistrements de l'objet **Recordset** actif sur la base de données sous-jacente. Ceci est utile si vous utilisez un curseur statique ou avant uniquement, mais que vous voulez afficher les modifications apportées dans la base de données sous-jacente.

Si vous affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, **Resync** n'est disponible que pour les objets **Recordset** en lecture-écriture.

Contrairement à la méthode [Requery](requery-method-ado.md), la méthode **Resync** ne réexécute pas la commande sous-jacente de l'objet **Recordset**. Les nouveaux enregistrements de la base de données sous-jacente ne seront pas visibles.

Si la tentative de resynchronisation échoue à cause d’un conflit avec les données sous-jacentes (par exemple, un enregistrement a été supprimé par un autre utilisateur), le fournisseur retourne des avertissements à la collection [Errors](errors-collection-ado.md) et une erreur d’exécution se produit. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) et [Status](status-property-ado-recordset.md) pour identifier les enregistrements qui créent des conflits.

Si les propriétés dynamiques [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et [Resync Command](resync-command-property-dynamic-ado.md) sont définies et que l'objet **Recordset** obtenu provient de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Resync** exécute la commande fournie dans la propriété **Resync Command** uniquement au niveau de la table désignée dans la propriété **Unique Table**.

### <a name="fields"></a>Champs

Faites appel à la méthode **Resync** pour resynchroniser les valeurs de la collection **Fields** d'un objet **Record** sur la source de données sous-jacente. La propriété [Count](count-property-ado.md) n'est pas affectée par cette méthode.

Si *ResyncValues* a la valeur **adResyncAllValues** (valeur par défaut), puis le [UnderlyingValue](underlyingvalue-property-ado.md), [valeur](value-property-ado.md)et propriétés [OriginalValue](originalvalue-property-ado.md) des objets [Field](field-object-ado.md) dans la collection sont synchronisées. Si *ResyncValues* a la valeur **adResyncUnderlyingValues**, seule la propriété **UnderlyingValue** est synchronisée.

La valeur de la propriété **Status** de chaque objet **Field** au moment de l’appel affecte également le comportement de **Resync**. Pour les objets **Field** avec les valeurs **d’état** **adFieldPendingUnknown** ou **adFieldPendingInsert**, **Resync** n’a aucun effet. Pour des valeurs **Status** **égales à adFieldPendingChange** ou **adFieldPendingDelete**, **elle** synchronise les valeurs de données pour les champs qui existent toujours dans la source de données.

**Resync** ne modifie pas les valeurs **d’état** d’objets **Field** , sauf si une erreur se produit **lorsqu’elle** est appelée. Par exemple, si le champ n’existe plus, le fournisseur retourne une valeur **Status** appropriée pour l’objet **Field** , comme **adFieldDoesNotExist**. Valeurs **d’état** renvoyées peuvent être associées logiquement dans la valeur de la propriété **Status** .

