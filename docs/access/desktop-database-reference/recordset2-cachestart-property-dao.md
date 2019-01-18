---
title: Propriété Recordset2.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718797"
---
# <a name="recordset2cachestart-property-dao"></a>Propriété Recordset2.CacheStart (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique contenant des données à mettre en cache local à partir d'une source de données ODBC (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . CacheStart

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

La mise en cache des données améliore les performances si vous utilisez des objets **Recordset** pour récupérer des données d'un serveur distant. Le cache est un espace en mémoire locale qui contient les données les plus récentes extraites du serveur. Il s'avère utile lorsque l'utilisateur demande à nouveau des données lors de l'exécution de l'application. En effet, lorsque l'utilisateur demande des données, le moteur de base de données Microsoft Access vérifie d'abord la présence des données demandées dans le cache, au lieu de les extraire du serveur, ce qui est plus long. Le cache n'enregistre que les données issues d'une source de données ODBC.

Toute source de données ODBC reliée à un moteur de base de données Microsoft Access (table liée, par exemple) peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante, définissez les propriétés **CacheSize** et **[CacheStart](recordset2-cachestart-property-dao.md)**, puis utilisez la méthode **[FillCache](recordset2-fillcache-method-dao.md)** ou parcourez les enregistrements à l'aide des méthodes **Move**.

La valeur de la propriété **CacheStart** correspond au signet du premier enregistrement dans l'objet **Recordset** à mettre en cache. Vous pouvez utiliser le signet de n'importe quel enregistrement pour définir la propriété **CacheStart**. Définissez l'enregistrement à placer au début du cache comme enregistrement actif et paramétrez la propriété **CacheStart** en fonction de la valeur de la propriété **[Bookmark](recordset2-bookmark-property-dao.md)**.

Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.

Les enregistrements extraits du cache ne répercutent pas les modifications apportées simultanément aux données sources par les autres utilisateurs.

Pour forcer la mise à jour de toutes les données mises en cache, définissez la propriété **CacheSize** de l'objet **Recordset** sur la valeur 0, redéfinissez-la en fonction de la taille du cache demandée à l'origine, puis utilisez la méthode **FillCache**.

