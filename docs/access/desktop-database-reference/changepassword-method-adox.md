---
title: ChangePassword, méthode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296527"
---
# <a name="changepassword-method-adox"></a>ChangePassword, méthode (ADOX)

**S’applique à** : Access 2013, Office 2013

Modifie le mot de passe d'un compte d'utilisateur.

## <a name="syntax"></a>Syntaxe

*User*. ChangePassword**, *newPassword, newPassword*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*OldPassword* |Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur. Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.|
|*NewPassword* |Valeur de type **String** qui spécifie le nouveau mot de passe.|

## <a name="remarks"></a>Remarques

Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.

Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.

