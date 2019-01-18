---
title: DataFactory, objet (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702179"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory, objet (RDSServer)


**S’applique à**: Access 2013, Office 2013

Cet objet métier côté serveur par défaut implémente des méthodes qui procurent un accès en lecture-écriture aux sources de données spécifiées pour des applications côté client.

## <a name="remarks"></a>Notes

L'objet **RDSServer.DataFactory** est conçu comme un objet Automation côté serveur, qui reçoit les demandes clientes. Dans une implémentation Internet, il réside sur un serveur web et est instancié par le composant ADISAPI. L'objet **RDSServer.DataFactory** fournit un accès en lecture-écriture aux sources de données spécifiées, mais ne contient pas de logique de validation ou de règles métier.

Si vous utilisez une méthode disponible à la fois pour les objets **RDSServer.DataFactory** et [RDS.DataControl](datacontrol-object-rds.md), Remote Data Service utilise la version **RDS.DataControl** par défaut. Un scénario de programmation de base est pris comme point de départ par défaut, **RDSServer.DataFactory** étant utilisé comme objet métier côté serveur générique.

Si vous souhaitez que votre application web gère le traitement du côté serveur spécifiques à la tâche, vous pouvez remplacer **RDSServer.DataFactory** par un objet métier personnalisé.

Vous pouvez créer des objets métier côté serveur qui appellent les méthodes de **RDSServer.DataFactory**, comme [Query](query-method-rds.md) et [CreateRecordset](createrecordset-method-rds.md). Cela s'avère utile si vous voulez ajouter des fonctionnalités à vos objets métier tout en profitant des technologies Remote Data Service existantes.

L'identificateur de classe de l'objet **RDSServer.DataFactory** est 9381D8F5-0288-11D0-9501-00AA00B911A5.

