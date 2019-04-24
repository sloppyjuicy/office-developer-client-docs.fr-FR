---
title: Événement FetchProgress, (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293181"
---
# <a name="fetchprogress-event-ado"></a>Événement FetchProgress, (ADO)

**S’applique à** : Access 2013, Office 2013

L’événement **FetchProgress** est régulièrement appelé pendant une opération asynchrone de longue durée, afin de signaler le nombre de lignes déjà extraites de l’objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Progression*FetchProgress,, *MaxProgress*, ** adStatus, *préobjet*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*Progress* |Valeur de type **Long** indiquant le nombre d'enregistrements déjà extraits par l'opération d'extraction.|
|*MaxProgress* |Valeur de type **Long** indiquant le nombre maximal prévu d'enregistrements à récupérer.|
|*Statu* |Valeur d'état [EventStatusEnum](eventstatusenum.md).|
|*jeu d'enregistrements* |Objet **Recordset** représentant le jeu duquel les enregistrements sont extraits.|

## <a name="remarks"></a>Remarques

En cas d’utilisation de **FetchProgress** avec un objet **Recordset** enfant, il est important de savoir que les valeurs des paramètres *Progress* et *MaxProgress* sont dérivées de l’ensemble de lignes du [service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md). Les valeurs retournées représentent le nombre total d’enregistrements de l’ensemble de lignes sous-jacent et pas seulement ceux du chapitre actif.

> [!NOTE]
> [!REMARQUE] Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchProgress** avec Microsoft Visual Basic.


