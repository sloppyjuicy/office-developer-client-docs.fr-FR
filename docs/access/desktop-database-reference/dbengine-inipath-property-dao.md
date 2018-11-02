---
title: Propriété DBEngine.IniPath (DAO)
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
ms.openlocfilehash: fd744f10d212d8ff0f7c78ca72781869ccdcd57e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928760"
---
# <a name="dbengineinipath-property-dao"></a>Propriété DBEngine.IniPath (DAO)


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

