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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713091"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="a73a0-102">ChangePassword, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a73a0-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="a73a0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a73a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a73a0-104">Modifie le mot de passe d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a73a0-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a73a0-105">Syntax</span></span>

<span data-ttu-id="a73a0-106">*Utilisateur*. De ChangePassword*Ancienmotdepasse*, groupes de *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="a73a0-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="a73a0-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a73a0-107">Parameters</span></span>

|<span data-ttu-id="a73a0-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a73a0-108">Parameter</span></span>|<span data-ttu-id="a73a0-109">Description</span><span class="sxs-lookup"><span data-stu-id="a73a0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a73a0-110">*Ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="a73a0-110">*OldPassword*</span></span> |<span data-ttu-id="a73a0-p101">Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur. Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="a73a0-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="a73a0-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="a73a0-113">*NewPassword*</span></span> |<span data-ttu-id="a73a0-114">Valeur de type **String** qui spécifie le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a73a0-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a73a0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a73a0-115">Remarks</span></span>

<span data-ttu-id="a73a0-116">Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a73a0-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="a73a0-117">Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.</span><span class="sxs-lookup"><span data-stu-id="a73a0-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

