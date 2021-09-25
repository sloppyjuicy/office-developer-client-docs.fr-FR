---
title: Workspace.LoginTimeout, propriété (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 841346da6d78389f52bc4c7882e5cfc8a0b0f945
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552373"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace.LoginTimeout, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie le nombre de secondes avant la survenue d’une erreur lorsque vous tentez de vous connecter à une base de données ODBC.

## <a name="syntax"></a>Syntaxe

*.* LoginTimeout

*expression* Variable qui représente un objet **Workspace**.

## <a name="remarks"></a>Remarques

La valeur de la propriété **LoginTimeout** est de 20 secondes par défaut. Si la propriété **LoginTimeout** a la valeur 0, il n'y a pas de délai imparti pour la connexion.

Si vous essayez de vous connecter à une base de données ODBC, comme Microsoft SQL Server, la connexion peut échouer suite à des erreurs réseau ou si le serveur ne fonctionne pas. Plutôt que d'attendre 20 secondes pour vous connecter, vous pouvez spécifier le temps d'attente avant l'apparition d'une erreur. La connexion au serveur s'effectue implicitement parmi une série d'événements, comme l'exécution d'une requête sur une base de données serveur externe.

