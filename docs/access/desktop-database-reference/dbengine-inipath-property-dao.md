---
title: DBEngine.IniPath, propriété (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: a84c27407ee370c406f791fa691d30fda3e79810
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585801"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie des informations sur la clé du Registre Windows contenant les valeurs relatives au moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* IniPath

*expression* Variable représentant un objet **DBEngine**.

## <a name="remarks"></a>Remarques

Vous pouvez configurer le moteur de base de données Microsoft Access avec Windows Registre. Ce dernier permet de définir des options comme les DLL ISAM installables.

Pour que cette option soit efficace, vous devez définir la propriété **IniPath** avant que votre application n'invoque un autre code DAO. L'étendue de ce paramètre est limitée à votre application et ne peut pas être modifiée sans redémarrer votre application.

Le Registre permet de fournir des paramètres d'initialisation pour certains pilotes de base de données ISAM installables. Par exemple, pour utiliser Paradox version 4.0, définissez la propriété **IniPath** sur une partie du Registre qui contient les paramètres appropriés.

Cette propriété reconnaît HKEY \_ LOCAL \_ MACHINE ou HKEY LOCAL \_ \_ USER. Si aucune clé racine n’est fournie, la valeur par défaut est HKEY \_ LOCAL \_ MACHINE.

