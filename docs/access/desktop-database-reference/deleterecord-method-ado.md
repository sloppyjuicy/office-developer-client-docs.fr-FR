---
title: DeleteRecord, méthode (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704517"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Supprime une entité représentée par un objet [Record](record-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Enregistrement*. **DeleteRecord *** Source*, *asynchrone*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **String** contenant l’URL qui identifie l’entité (par exemple, le fichier ou le répertoire) à supprimer. Si le paramètre *Source* est omis ou spécifie une chaîne vide, l’entité représentée par l’objet [Record](record-object-ado.md) actif est supprimée. Si l’objet Record est un enregistrement de collection (propriété [RecordType](recordtype-property-ado.md) avec la valeur **adCollectionRecord**, tel qu’un répertoire) tous les enfants (par exemple les sous-répertoires) seront également supprimés.|
|*Async* |Facultatif. Valeur de type **Boolean**. Si sa valeur est **True**, spécifie que l'opération de suppression est asynchrone.|

## <a name="remarks"></a>Notes

Opérations sur l’objet représenté par cet **enregistrement** peuvent échouer une fois cette méthode terminée. Après avoir appelé **DeleteRecord**, l' **enregistrement** doit être fermé car le comportement de l' **enregistrement** peut devenir imprévisible selon le moment où le fournisseur met à jour l' **enregistrement** de la source de données.

Si cet **enregistrement** a été obtenue à partir d’un [jeu d’enregistrements](recordset-object-ado.md), puis les résultats de cette opération ne seront pas reflétées immédiatement dans le **jeu d’enregistrements**. Actualiser le **jeu d’enregistrements** en fermant et en ouvrant de nouveau ou en exécutant les méthodes **Recordset** [Requery](requery-method-ado.md)ou [Update](update-method-ado.md) et [Resync](resync-method-ado.md) .

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).


