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
# <a name="resync-method-ado"></a><span data-ttu-id="2de4b-102">Resync, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2de4b-102">Resync method (ADO)</span></span>

<span data-ttu-id="2de4b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2de4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2de4b-104">Cette méthode actualise les données de l’objet [Recordset](recordset-object-ado.md) actif ou la collection [Fields](fields-collection-ado.md) d’un objet [Record](record-object-ado.md) à partir de la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="2de4b-104">Refreshes the data in the current [Recordset](recordset-object-ado.md) object, or [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, from the underlying database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de4b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2de4b-105">Syntax</span></span>

<span data-ttu-id="2de4b-106">*Recordset*. Resync *AffectRecords*, *ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="2de4b-106">*Recordset*.Resync *AffectRecords*, *ResyncValues*</span></span>

<span data-ttu-id="2de4b-107">*Enregistrement*.</span><span class="sxs-lookup"><span data-stu-id="2de4b-107">*Record*.</span></span> <span data-ttu-id="2de4b-108">*Champs*. Resync *ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="2de4b-108">*Fields*.Resync *ResyncValues*</span></span>

## <a name="parameters"></a><span data-ttu-id="2de4b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2de4b-109">Parameters</span></span>

|<span data-ttu-id="2de4b-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2de4b-110">Parameter</span></span>|<span data-ttu-id="2de4b-111">Description</span><span class="sxs-lookup"><span data-stu-id="2de4b-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2de4b-112">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="2de4b-112">*AffectRecords*</span></span> |<span data-ttu-id="2de4b-p102">Facultatif. La valeur [AffectEnum](affectenum.md) détermine combien d'enregistrements sont affectés par la méthode **Resync**. La valeur **adAffectAll** est utilisée par défaut ; elles n'est pas disponible avec la méthode **Resync** de la collection **Fields** d'un objet **Record**.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p102">Optional. An [AffectEnum](affectenum.md) value that determines how many records the **Resync** method will affect. The default value is **adAffectAll**. This value is not available with the **Resync** method of the **Fields** collection of a **Record** object.</span></span>|
|<span data-ttu-id="2de4b-117">*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="2de4b-117">*ResyncValues*</span></span> |<span data-ttu-id="2de4b-p103">Facultatif. La valeur [ResyncEnum](resyncenum.md) indique si les valeurs sous-jacentes sont remplacées. La valeur par défaut est **adResyncAllValues**.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p103">Optional. A [ResyncEnum](resyncenum.md) value that specifies whether underlying values are overwritten. The default value is **adResyncAllValues**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2de4b-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="2de4b-121">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="2de4b-122">Recordset</span><span class="sxs-lookup"><span data-stu-id="2de4b-122">Recordset</span></span>

<span data-ttu-id="2de4b-p104">Faites appel à la méthode **Resync** pour resynchroniser des enregistrements de l'objet **Recordset** actif sur la base de données sous-jacente. Ceci est utile si vous utilisez un curseur statique ou avant uniquement, mais que vous voulez afficher les modifications apportées dans la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p104">Use the **Resync** method to resynchronize records in the current **Recordset** with the underlying database. This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</span></span>

<span data-ttu-id="2de4b-125">Si vous affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, **Resync** n'est disponible que pour les objets **Recordset** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2de4b-125">If you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**, **Resync** is only available for non-read-only **Recordset** objects.</span></span>

<span data-ttu-id="2de4b-p105">Contrairement à la méthode [Requery](requery-method-ado.md), la méthode **Resync** ne réexécute pas la commande sous-jacente de l'objet **Recordset**. Les nouveaux enregistrements de la base de données sous-jacente ne seront pas visibles.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p105">Unlike the [Requery](requery-method-ado.md) method, the **Resync** method does not re-execute the **Recordset** object's underlying command. New records in the underlying database will not be visible.</span></span>

<span data-ttu-id="2de4b-p106">Si la tentative de resynchronisation échoue à cause d’un conflit avec les données sous-jacentes (par exemple, un enregistrement a été supprimé par un autre utilisateur), le fournisseur retourne des avertissements à la collection [Errors](errors-collection-ado.md) et une erreur d’exécution se produit. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) et [Status](status-property-ado-recordset.md) pour identifier les enregistrements qui créent des conflits.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p106">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterConflictingRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="2de4b-130">Si les propriétés dynamiques [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et [Resync Command](resync-command-property-dynamic-ado.md) sont définies et que l'objet **Recordset** obtenu provient de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Resync** exécute la commande fournie dans la propriété **Resync Command** uniquement au niveau de la table désignée dans la propriété **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="2de4b-130">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Resync Command](resync-command-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Resync** method will execute the command given in the **Resync Command** property only on the table named in the **Unique Table** property.</span></span>

### <a name="fields"></a><span data-ttu-id="2de4b-131">Champs</span><span class="sxs-lookup"><span data-stu-id="2de4b-131">Fields</span></span>

<span data-ttu-id="2de4b-p107">Faites appel à la méthode **Resync** pour resynchroniser les valeurs de la collection **Fields** d’un objet **Record** sur la source de données sous-jacente. La propriété [Count](count-property-ado.md) n’est pas affectée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p107">Use the **Resync** method to resynchronize the values of the **Fields** collection of a **Record** object with the underlying data source. The [Count](count-property-ado.md) property is not affected by this method.</span></span>

<span data-ttu-id="2de4b-p108">Si *ResyncValues* a la valeur par défaut **adResyncAllValues**, les propriétés [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md) et [OriginalValue](originalvalue-property-ado.md) des objets [Field](field-object-ado.md) de la collection sont synchronisés. Si *ResyncValues* a la valeur **adResyncUnderlyingValues**, seule la propriété **UnderlyingValue** est synchronisée.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p108">If *ResyncValues* is set to **adResyncAllValues** (the default value), then the [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md), and [OriginalValue](originalvalue-property-ado.md) properties of [Field](field-object-ado.md) objects in the collection are synchronized. If *ResyncValues* is set to **adResyncUnderlyingValues**, only the **UnderlyingValue** property is synchronized.</span></span>

<span data-ttu-id="2de4b-p109">The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**. For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect. For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p109">The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**. For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect. For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.</span></span>

<span data-ttu-id="2de4b-p110">**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.</span><span class="sxs-lookup"><span data-stu-id="2de4b-p110">**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.</span></span>

