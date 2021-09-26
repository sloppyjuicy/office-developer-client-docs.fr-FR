---
title: CancelBatch, méthode (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4e217ef575dc4538e76faf48669b746d2b8b60de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606981"
---
# <a name="cancelbatch-method-ado"></a>CancelBatch, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Annule une mise à jour par lot en attente.

## <a name="syntax"></a>Syntaxe

*recordset*. CancelBatch *AffectRecords*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*AffectRecords* |Facultatif. Valeur [AffectEnum](affectenum.md) qui indique le nombre d'enregistrements affectés par la méthode **CancelBatch**. |

## <a name="remarks"></a>Remarques

Utilisez la méthode **CancelBatch** pour annuler toutes les mises à jour en attente dans un objet [Recordset](recordset-object-ado.md) en mode de mise à jour par lot. Si l'objet **Recordset** est en mode de mise à jour immédiate, l'appel de la méthode **CancelBatch** sans **adAffectCurrent** génère une erreur.

Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **CancelBatch**, ADO commence par appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) pour annuler les modifications mises en cache. Ensuite, toutes les modifications en attente dans l'objet **Recordset** sont annulées.

Il se peut que l'enregistrement actif ne puisse pas être déterminé après un appel de la méthode **CancelBatch**, notamment si vous étiez en train d'ajouter un nouvel enregistrement. C'est pourquoi il est conseillé de définir la position de l'enregistrement actif à un emplacement connu de l'objet **Recordset** après avoir appelé la méthode **CancelBatch**. Appelez, par exemple, la méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

Si la tentative d’annulation des mises à jour en attente échoue à cause d’un conflit avec les données sous-jacentes (par exemple, un enregistrement a été supprimé par un autre utilisateur), le fournisseur retourne des avertissements dans la collection [Errors](errors-collection-ado.md), mais n’interrompt pas l’exécution. Une erreur d’exécution ne se produit qu’en cas de conflits dans tous les enregistrements demandés. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) et [Status](status-property-ado-recordset.md) pour localiser les enregistrements en conflit.

