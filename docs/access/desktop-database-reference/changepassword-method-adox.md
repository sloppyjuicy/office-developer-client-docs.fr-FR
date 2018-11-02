---
title: ChangePassword, méthode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f11cfaddc99a0e10a86e0df9a7a187c4e89fc794
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921060"
---
# <a name="changepassword-method-adox"></a>ChangePassword, méthode (ADOX)


**S’applique à**: Access 2013, Office 2013



Modifie le mot de passe d'un compte d'utilisateur.

## <a name="syntax"></a>Syntaxe

*Utilisateur*. De ChangePassword*Ancienmotdepasse*, groupes de *NewPassword*

## <a name="parameters"></a>Paramètres

  - *Ancienmotdepasse*

  - Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur. Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.

  - *NewPassword*

  - Valeur de type **String** qui spécifie le nouveau mot de passe.

## <a name="remarks"></a>Notes

Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.

Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.

