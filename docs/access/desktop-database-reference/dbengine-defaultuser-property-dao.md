---
title: DBEngine.DefaultUser, propriété (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 4b6a8a8f65b450d38a820bd00468cbde38facbd6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585815"
---
# <a name="dbenginedefaultuser-property-dao"></a>DBEngine.DefaultUser, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit le nom d'utilisateur servant à créer l'objet **Workspace** par défaut lors de son initialisation. Valeur de type **String** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*.* DefaultUser

*expression* Expression renvoyant un objet **DBEngine**.

## <a name="remarks"></a>Remarques

Le paramètre **defaultUser est** un type de données String. Elle peut comporter de 1 à 20 caractères dans les espaces de travail Microsoft Access et peut inclure des caractères alphabétiques, des caractères accentués, des nombres, des espaces et des symboles à l’exception de : " (guillemets), / (barre oblique \\ inverse), \[ \] (barres obliques inverses), (crochets), : (deux-points), | (pipe), \< (less-than sign), \> (signe supérieur à), + (signe plus), = (signe égal), ; (point-virgule), , ( virgule), ? (point d’interrogation), (astérisque), espaces de tête et caractères de contrôle \* (ASCII 00 à ASCII 31).


> [!NOTE]
> [!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.

Par défaut, la propriété **DefaultUser** est définie sur « admin » et la propriété **DefaultPassword** est définie sur une chaîne nulle ("").

En règle générale, les noms d'utilisateur ne respectent pas la casse. Toutefois, si vous recréez un compte d'utilisateur qui a été supprimé ou créé dans un autre groupe de travail, les minuscules et les majuscules du nom d'utilisateur doivent correspondre exactement à celles du nom d'origine. Les mots de passe respectent la casse.

En règle générale, vous utilisez la méthode **CreateWorkspace** pour créer un objet **Workspace** en fonction d'un nom d'utilisateur et d'un mot de passe spécifiques. Toutefois, pour des raisons de compatibilité descendante avec les versions antérieures et de commodité lorsque vous n'implémentez pas de base de données sécurisée, le moteur de base de données Microsoft Access crée automatiquement un objet **Workspace** par défaut s'il n'est pas encore ouvert. Dans ce cas, les valeurs des propriétés **DefaultUser** et **DefaultPassword** définissent l'utilisateur et le mot de passe correspondant à l'objet **Workspace** par défaut.

Pour appliquer cette propriété, vous devez la définir avant d'appeler des méthodes DAO.

