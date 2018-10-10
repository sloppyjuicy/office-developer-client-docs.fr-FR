---
title: DBEngine.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 53df33e3171cde0d861f738a852350ec20bf0dec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470247"
---
# <a name="dbenginelogintimeout-property-dao"></a>DBEngine.LoginTimeout Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie le nombre de secondes devant s'écouler avant l'apparition d'une erreur lorsque vous essayez de vous connecter à une base de données ODBC.

## <a name="syntax"></a>Syntaxe

*expression* . LoginTimeout

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

La valeur de la propriété **LoginTimeout** est de 20 secondes par défaut. Si la propriété **LoginTimeout** a la valeur 0, il n'y a pas de délai imparti pour la connexion.

Si vous essayez de vous connecter à une base de données ODBC, comme Microsoft SQL Server, la connexion peut échouer suite à des erreurs réseau ou si le serveur ne fonctionne pas. Plutôt que d'attendre 20 secondes pour vous connecter, vous pouvez spécifier le temps d'attente avant l'apparition d'une erreur. La connexion au serveur s'effectue implicitement parmi une série d'événements, comme l'exécution d'une requête sur une base de données serveur externe.

