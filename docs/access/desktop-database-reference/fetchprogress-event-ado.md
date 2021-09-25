---
title: FetchProgress, événement (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 32aca282a3ef79ad5e29614445559a653034528a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602670"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress, événement (ADO)

**S’applique à** : Access 2013, Office 2013

L’événement **FetchProgress** est régulièrement appelé pendant une opération asynchrone de longue durée, afin de signaler le nombre de lignes déjà extraites de l’objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Progress* |Valeur de type **Long** indiquant le nombre d'enregistrements déjà extraits par l'opération d'extraction.|
|*MaxProgress* |Valeur de type **Long** indiquant le nombre maximal prévu d'enregistrements à récupérer.|
|*adStatus* |Valeur d'état [EventStatusEnum](eventstatusenum.md).|
|*pRecordset* |Objet **Recordset** représentant le jeu duquel les enregistrements sont extraits.|

## <a name="remarks"></a>Remarques

En cas d’utilisation de **FetchProgress** avec un objet **Recordset** enfant, il est important de savoir que les valeurs des paramètres *Progress* et *MaxProgress* sont dérivées de l’ensemble de lignes du [service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md). Les valeurs retournées représentent le nombre total d’enregistrements de l’ensemble de lignes sous-jacent et pas seulement ceux du chapitre actif.

> [!NOTE]
> [!REMARQUE] Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchProgress** avec Microsoft Visual Basic.


