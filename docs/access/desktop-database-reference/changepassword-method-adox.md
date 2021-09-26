---
title: ChangePassword, méthode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5fdc08b191e735ddcad0b9dae9962cb657521993
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590092"
---
# <a name="changepassword-method-adox"></a>ChangePassword, méthode (ADOX)

**S’applique à** : Access 2013, Office 2013

Modifie le mot de passe d'un compte d'utilisateur.

## <a name="syntax"></a>Syntaxe

*Utilisateur*. ChangePassword *OldPassword*, *NewPassword*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*OldPassword* |Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur. Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.|
|*NewPassword* |Valeur de type **String** qui spécifie le nouveau mot de passe.|

## <a name="remarks"></a>Remarques

Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.

Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.

