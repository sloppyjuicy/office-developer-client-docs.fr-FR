---
title: ChangePassword, méthode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7eef5fc93f9cce68e6342b62c1ab07ee6f65587f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946019"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="4ba09-102">ChangePassword, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4ba09-102">ChangePassword method (ADOX)</span></span>


<span data-ttu-id="4ba09-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ba09-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="4ba09-104">Modifie le mot de passe d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ba09-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ba09-105">Syntax</span></span>

<span data-ttu-id="4ba09-106">*Utilisateur*. De ChangePassword*Ancienmotdepasse*, groupes de *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="4ba09-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="4ba09-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ba09-107">Parameters</span></span>

- <span data-ttu-id="4ba09-108">*Ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="4ba09-108">*OldPassword*</span></span>

  - <span data-ttu-id="4ba09-p101">Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur. Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="4ba09-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

- <span data-ttu-id="4ba09-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="4ba09-111">*NewPassword*</span></span>

  - <span data-ttu-id="4ba09-112">Valeur de type **String** qui spécifie le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4ba09-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba09-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4ba09-113">Remarks</span></span>

<span data-ttu-id="4ba09-114">Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4ba09-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="4ba09-115">Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.</span><span class="sxs-lookup"><span data-stu-id="4ba09-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

