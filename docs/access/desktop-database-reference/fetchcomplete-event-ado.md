---
title: FetchComplete, événement (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701962"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete, événement (ADO)

**S’applique à**: Access 2013, Office 2013

L'événement **FetchComplete** est appelé après que tous les enregistrements d'une longue opération asynchrone aient été extraits de l'objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

FetchComplete*pError*, *adStatus*, *Connection*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.|
|*Connection* |Objet **Recordset** représentant le jeu duquel les enregistrements ont été extraits.|

## <a name="remarks"></a>Notes

Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchComplete** avec Microsoft Visual Basic.

