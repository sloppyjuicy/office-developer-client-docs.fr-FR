---
title: onReadyStateChange, événement (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869231"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange, événement (RDS)


**S’applique à**: Access 2013, Office 2013


L'événement **onReadyStateChange** est appelé chaque fois que la valeur de la propriété [ReadyState](readystate-property-rds.md) est modifiée.

## <a name="syntax"></a>Syntaxe

onReadyStateChange

## <a name="parameters"></a>Paramètres

Aucun.

## <a name="remarks"></a>Notes

La propriété **ReadyState** reflète la progression de l'opération de récupération des données asynchrone effectuée par un objet [RDS.DataControl](datacontrol-object-rds.md) dans son objet [Recordset](recordset-object-ado.md). L'événement **onReadyStateChange** permet de suivre les modifications apportées à la propriété **ReadyState**. Cette méthode s'avère plus efficace qu'un contrôle périodique de la valeur de la propriété.

