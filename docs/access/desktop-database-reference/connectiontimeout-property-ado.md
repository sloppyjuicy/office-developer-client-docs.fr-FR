---
title: ConnectionTimeout, propriété (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700933"
---
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique le délai d'attente pour l'établissement d'une connexion avant l'abandon de la tentative et la génération d'une erreur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** indiquant, en secondes, le délai d'attente pour l'ouverture d'une connexion. La valeur par défaut est 15.

## <a name="remarks"></a>Notes

Utilisez la propriété **ConnectionTimeout** dans un objet [Connection](connection-object-ado.md) si des retards dus au trafic réseau ou à une utilisation intensive du serveur imposent d'abandonner une tentative de connexion. Si le délai défini dans la propriété **ConnectionTimeout** s'écoule avant l'ouverture de la connexion, une erreur est générée et ADO annule la tentative. Si vous attribuez la valeur zéro à la propriété, ADO attend indéfiniment jusqu'à ce que la connexion soit ouverte. Assurez-vous que le fournisseur dans lequel vous écrivez le code prend en charge la fonctionnalité **ConnectionTimeout**.

La propriété **ConnectionTimeout** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte.

