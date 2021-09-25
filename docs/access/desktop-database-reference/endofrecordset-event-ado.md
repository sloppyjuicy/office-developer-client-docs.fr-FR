---
title: EndOfRecordset, événement (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 336dd8f5dce734e7b820f8bf78f113d122d90444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602751"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset, événement (ADO)

**S’applique à** : Access 2013, Office 2013

L’événement **EndOfRecordset** est appelé lors d’une tentative de positionnement sur une ligne au-delà de la fin d’un objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*fMoreData* |Valeur **\_ BOOL VARIANT** qui, si elle est définie sur VARIANT TRUE, indique que d’autres lignes ont été \_ ajoutées au jeu **d’enregistrements.**|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **EndOfRecordset** est appelé, ce paramètre est paramétré sur **adStatusOK** si l’opération à l’origine de l’événement a réussi. Elle est définie sur **adStatusCantDeny** si cet événement ne peut pas demander l’annulation de l’opération à l’origine de cet événement.<br/><br/>Avant que **EndOfRecordset** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.|
|*pRecordset* | A **Recordset** object. The **Recordset** for which this event occurred.|

## <a name="remarks"></a>Remarques

Un événement **EndOfRecordset** peut être généré si l'opération [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) échoue.

Ce gestionnaire d'événements est appelé lors d'une tentative de positionnement au-delà de la fin de l'objet **Recordset**, résultant probablement d'un appel à **MoveNext**. À partir de l'événement, il est toujours possible toutefois de récupérer plusieurs enregistrements d'une base de données et de les ajouter à la fin de l'objet **Recordset**. Dans ce cas, définissez *fMoreData* sur VARIANT \_ TRUE et revenir de **EndOfRecordset**. Rappelez ensuite **MoveNext** pour accéder aux nouveaux enregistrements récupérés.

