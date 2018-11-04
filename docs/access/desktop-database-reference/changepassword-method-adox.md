---
title: ChangePassword, méthode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7e6d88b207fecc93b9a9bafa2d6b504456a3a3e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949270"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="fe8ee-102">ChangePassword, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fe8ee-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="fe8ee-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe8ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe8ee-104">Modifie le mot de passe d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fe8ee-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe8ee-105">Syntax</span></span>

<span data-ttu-id="fe8ee-106">*Utilisateur*. De ChangePassword*Ancienmotdepasse*, groupes de *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="fe8ee-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="fe8ee-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe8ee-107">Parameters</span></span>

|<span data-ttu-id="fe8ee-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fe8ee-108">Parameter</span></span>|<span data-ttu-id="fe8ee-109">Description</span><span class="sxs-lookup"><span data-stu-id="fe8ee-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fe8ee-110">*Ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="fe8ee-110">*OldPassword*</span></span> |<span data-ttu-id="fe8ee-p101">Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur. Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="fe8ee-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="fe8ee-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="fe8ee-113">*NewPassword*</span></span> |<span data-ttu-id="fe8ee-114">Valeur de type **String** qui spécifie le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fe8ee-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fe8ee-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fe8ee-115">Remarks</span></span>

<span data-ttu-id="fe8ee-116">Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fe8ee-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="fe8ee-117">Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.</span><span class="sxs-lookup"><span data-stu-id="fe8ee-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

