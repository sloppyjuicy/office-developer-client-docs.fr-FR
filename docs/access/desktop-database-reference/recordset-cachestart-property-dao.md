---
title: Recordset.CacheStart, propriété (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300615"
---
# <a name="recordsetcachestart-property-dao"></a>Recordset.CacheStart, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur spécifiant le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique qui contient des données d'une source de données ODBC à placer dans le cache local (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* CacheStart

*expression* Variable qui représente un objet **Recordset**.

## <a name="remarks"></a>Remarques

La mise en cache des données améliore les performances si vous utilisez des objets **Recordset** pour extraire des données d'un serveur distant. Un cache est un espace de la mémoire locale qui conserve les données récemment extraites du serveur. La mise en cache est utile si les utilisateurs demandent à nouveau les données au cours de la même session d'application. En cas de demande des données, le moteur de base de données Microsoft Access vérifie si les données demandées figurent dans le cache avant de tenter de les récupérer auprès du serveur, ce qui prend plus longtemps. Le cache enregistre uniquement des données issues d'une source de données ODBC.

N'importe quelle source de données ODBC connectée au moteur de base de données Microsoft Access, telle qu'une table liée, peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante, définissez les propriétés **CacheSize** et **[CacheStart](recordset-cachestart-property-dao.md)** puis utilisez la méthode **[FillCache](recordset-fillcache-method-dao.md)** ou parcourez les enregistrements à l'aide des méthodes **Move**.

Le paramètre de la propriété **CacheStart** est le signet du premier enregistrement de l'objet **Recordset** à mettre en cache. Vous pouvez utiliser le signet d'un enregistrement quelconque pour définir la propriété **CacheStart**. Définissez en tant qu'enregistrement actif le premier enregistrement à mettre en cache et affectez à la propriété **CacheStart** la même valeur que la propriété **[Bookmark](recordset-bookmark-property-dao.md)**.

Le moteur de base de données Microsoft Access demande au cache les enregistrements compris dans la plage du cache et demande au serveur les enregistrements hors cache.

Les enregistrements extraits du cache ne reflètent pas les modifications apportées simultanément par d'autres utilisateurs à la source de données.

Pour forcer une mise à jour de toutes les données mises en cache, affectez à la propriété **CacheSize** de l'objet **Recordset** la valeur 0, réaffectez-lui une valeur correspondant à la taille du cache initialement demandé puis utilisez la méthode **FillCache**.

