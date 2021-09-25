---
title: DeleteRecord, méthode (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8d8107acb9a4335bf0635117bb57626f6a971e24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565512"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Supprime une entité représentée par un objet [Record](record-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Enregistrement*. **DeleteRecord**_Source_, *Async*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **String** contenant l’URL qui identifie l’entité (par exemple, le fichier ou le répertoire) à supprimer. Si le paramètre *Source* est omis ou spécifie une chaîne vide, l’entité représentée par l’objet [Record](record-object-ado.md) actif est supprimée. Si l’objet Record est un enregistrement de collection (propriété [RecordType](recordtype-property-ado.md) avec la valeur **adCollectionRecord**, tel qu’un répertoire) tous les enfants (par exemple les sous-répertoires) seront également supprimés.|
|*Async* |Facultatif. Valeur de type **Boolean**. Si sa valeur est **True**, spécifie que l'opération de suppression est asynchrone.|

## <a name="remarks"></a>Remarques

Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.

If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**. **Actualisez le recordset** en le fermant et en le ré ouvrant, ou en exécutant la méthode [Requery](requery-method-ado.md)ou [Update](update-method-ado.md) et [Resync.](resync-method-ado.md) 

> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)


