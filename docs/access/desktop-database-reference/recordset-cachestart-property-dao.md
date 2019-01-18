---
title: Propriété Recordset.CacheStart (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699984"
---
# <a name="recordsetcachestart-property-dao"></a>Propriété Recordset.CacheStart (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique contenant des données à mettre en cache local à partir d'une source de données ODBC (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . CacheStart

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

La mise en cache des données améliore les performances si vous utilisez des objets **Recordset** pour récupérer des données d'un serveur distant. Le cache est un espace en mémoire locale qui contient les données les plus récentes extraites du serveur. Il s'avère utile lorsque l'utilisateur demande à nouveau des données lors de l'exécution de l'application. En effet, lorsque l'utilisateur demande des données, le moteur de base de données Microsoft Access vérifie d'abord la présence des données demandées dans le cache, au lieu de les extraire du serveur, ce qui est plus long. Le cache n'enregistre que les données issues d'une source de données ODBC.

Toute source de données ODBC reliée à un moteur de base de données Microsoft Access (table liée, par exemple) peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante, définissez les propriétés **CacheSize** et **[CacheStart](recordset-cachestart-property-dao.md)**, puis utilisez la méthode **[FillCache](recordset-fillcache-method-dao.md)** ou parcourez les enregistrements à l'aide des méthodes **Move**.

La valeur de la propriété **CacheStart** correspond au signet du premier enregistrement dans l'objet **Recordset** à mettre en cache. Vous pouvez utiliser le signet de n'importe quel enregistrement pour définir la propriété **CacheStart**. Définissez l'enregistrement à placer au début du cache comme enregistrement actif et paramétrez la propriété **CacheStart** en fonction de la valeur de la propriété **[Bookmark](recordset-bookmark-property-dao.md)**.

Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.

Les enregistrements extraits du cache ne répercutent pas les modifications apportées simultanément aux données sources par les autres utilisateurs.

Pour forcer la mise à jour de toutes les données mises en cache, définissez la propriété **CacheSize** de l'objet **Recordset** sur la valeur 0, redéfinissez-la en fonction de la taille du cache demandée à l'origine, puis utilisez la méthode **FillCache**.

