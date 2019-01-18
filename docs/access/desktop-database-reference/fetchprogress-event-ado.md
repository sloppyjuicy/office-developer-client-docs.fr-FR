---
title: FetchProgress, événement (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703516"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress, événement (ADO)

**S’applique à**: Access 2013, Office 2013

L'événement **FetchProgress** est régulièrement appelé pendant une opération asynchrone de longue durée, afin de signaler le nombre de lignes déjà extraites de l'objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

FetchProgress*progression*, *MaxProgress*, *adStatus*, *Connection*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Progress* |Valeur de type **Long** indiquant le nombre d'enregistrements déjà extraits par l'opération d'extraction.|
|*MaxProgress* |Valeur de type **Long** indiquant le nombre maximal prévu d'enregistrements à récupérer.|
|*adStatus* |Valeur d'état [EventStatusEnum](eventstatusenum.md).|
|*Connection* |Objet **Recordset** représentant le jeu duquel les enregistrements sont extraits.|

## <a name="remarks"></a>Notes

Lorsque vous utilisez **FetchProgress** avec un **objet Recordset**enfant, n’oubliez pas que les valeurs des paramètres *Progress* et *MaxProgress* sont dérivées de l’ensemble de lignes [Service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md) sous-jacent. Les valeurs retournées représentent le nombre total d'enregistrements de l'ensemble de lignes sous-jacent et pas seulement ceux du chapitre actif.

> [!NOTE]
> [!REMARQUE] Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchProgress** avec Microsoft Visual Basic.


