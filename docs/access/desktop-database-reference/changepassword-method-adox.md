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
# <a name="changepassword-method-adox"></a><span data-ttu-id="f970b-102">ChangePassword, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f970b-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="f970b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f970b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f970b-104">Modifie le mot de passe d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f970b-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="f970b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f970b-105">Syntax</span></span>

<span data-ttu-id="f970b-106">*Utilisateur*. ChangePassword *OldPassword*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="f970b-106">*User*.ChangePassword *OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="f970b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f970b-107">Parameters</span></span>

|<span data-ttu-id="f970b-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f970b-108">Parameter</span></span>|<span data-ttu-id="f970b-109">Description</span><span class="sxs-lookup"><span data-stu-id="f970b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f970b-110">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="f970b-110">*OldPassword*</span></span> |<span data-ttu-id="f970b-111">Valeur de type **String** qui spécifie le mot de passe existant de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f970b-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="f970b-112">Si l'utilisateur ne possède pas de mot de passe, utilisez une chaîne vide ("") pour le paramètre *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="f970b-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="f970b-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="f970b-113">*NewPassword*</span></span> |<span data-ttu-id="f970b-114">Valeur de type **String** qui spécifie le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f970b-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f970b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="f970b-115">Remarks</span></span>

<span data-ttu-id="f970b-116">Pour des raisons de sécurité, l'ancien mot de passe doit être spécifié en plus du nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f970b-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="f970b-117">Une erreur se produit si le fournisseur ne prend pas en charge l'administration de propriétés d'approbation.</span><span class="sxs-lookup"><span data-stu-id="f970b-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

