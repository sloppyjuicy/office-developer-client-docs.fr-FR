---
title: Propriété DBEngine.DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704734"
---
# <a name="dbenginedefaultpassword-property-dao"></a>Propriété DBEngine.DefaultPassword (DAO)


**S’applique à**: Access 2013, Office 2013

Définit le mot de passe servant à créer l'objet **Workspace** par défaut lors de son initialisation. Valeur de type **String** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . DefaultPassword

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

La valeur de la propriété **DefaultPassword** est une donnée de type String qui peut contenir jusqu'à 20 caractères. Elle accepte tous les caractères, à l'exception du caractère ASCII 0.


> [!NOTE]
> [!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.

Par défaut, la propriété **DefaultUser** est définie sur « admin » et la propriété **DefaultPassword** est définie sur une chaîne nulle ("").

En règle générale, vous utilisez la méthode **CreateWorkspace** pour créer un objet **Workspace** en fonction d'un nom d'utilisateur et d'un mot de passe spécifiques. Toutefois, pour des raisons de compatibilité descendante avec les versions antérieures et de commodité lorsque vous n'implémentez pas de base de données sécurisée, le moteur de base de données Microsoft Access crée automatiquement un objet **Workspace** par défaut s'il n'est pas encore ouvert. Dans ce cas, les valeurs des propriétés **DefaultUser** et **DefaultPassword** définissent l'utilisateur et le mot de passe correspondant à l'objet **Workspace** par défaut.

Pour appliquer cette propriété, vous devez la définir avant d'appeler des méthodes DAO.

