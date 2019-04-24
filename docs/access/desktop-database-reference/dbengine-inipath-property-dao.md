---
title: DBEngine. IniPath, propriété (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294294"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine. IniPath, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie des informations sur la clé du Registre Windows contenant les valeurs relatives au moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . IniPath

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

Vous pouvez configurer le moteur de base de données Microsoft Access avec le Registre Windows. Ce dernier permet de définir des options comme les DLL ISAM installables.

Pour que cette option soit efficace, vous devez définir la propriété **IniPath** avant que votre application n'invoque un autre code DAO. L'étendue de ce paramètre est limitée à votre application et ne peut pas être modifiée sans redémarrer votre application.

Le Registre permet de fournir des paramètres d'initialisation pour certains pilotes de base de données ISAM installables. Par exemple, pour utiliser Paradox version 4.0, définissez la propriété **IniPath** sur une partie du Registre qui contient les paramètres appropriés.

Cette propriété reconnaît soit HKEY\_local\_machine, soit\_HKEY\_local User. Si aucune clé racine n'est fournie, la valeur par\_défaut\_est HKEY local machine.

