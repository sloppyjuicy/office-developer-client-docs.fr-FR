---
title: DBEngine.IniPath Property (DAO)
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
ms.openlocfilehash: 344f5b0a1edac379386208a831d332e8926654ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882958"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath Property (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie des informations sur la clé du Registre Windows contenant les valeurs relatives au moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . IniPath

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

Vous pouvez configurer le moteur de base de données Microsoft Access avec le Registre Windows. Ce dernier permet de définir des options comme les DLL ISAM installables.

Pour que cette option soit efficace, vous devez définir la propriété **IniPath** avant que votre application n'invoque un autre code DAO. L'étendue de ce paramètre est limitée à votre application et ne peut pas être modifiée sans redémarrer votre application.

Le Registre permet de fournir des paramètres d'initialisation pour certains pilotes de base de données ISAM installables. Par exemple, pour utiliser Paradox version 4.0, définissez la propriété **IniPath** sur une partie du Registre qui contient les paramètres appropriés.

Cette propriété reconnaît soit HKEY\_LOCAL\_MACHINE ou HKEY\_LOCAL\_utilisateur. Si aucune clé racine n’est fourni, la valeur par défaut est HKEY\_LOCAL\_MACHINE.

