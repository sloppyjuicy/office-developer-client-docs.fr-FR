---
title: onReadyStateChange, événement (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e52ef236a5e57efc965a6b3bd8ab6edd7533f2c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922208"
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

