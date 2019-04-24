---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338408"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="bbf9c-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="bbf9c-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="bbf9c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbf9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbf9c-105">Renvoie une table des modèles uniques permettant de créer des destinataires à ajouter à la liste des destinataires d'un message sortant.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="bbf9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbf9c-106">Parameters</span></span>

 <span data-ttu-id="bbf9c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbf9c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bbf9c-108">dans Masque de des indicateurs qui contrôle le type de colonnes de chaîne incluses dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="bbf9c-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="bbf9c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bbf9c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bbf9c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bbf9c-111">Les colonnes de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="bbf9c-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="bbf9c-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="bbf9c-113">_lppTable_</span></span>
  
> <span data-ttu-id="bbf9c-114">remarquer Pointeur vers un pointeur vers la table ponctuelle.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbf9c-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bbf9c-115">Return value</span></span>

<span data-ttu-id="bbf9c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbf9c-116">S_OK</span></span> 
  
> <span data-ttu-id="bbf9c-117">La table ponctuelle a été récupérée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="bbf9c-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bbf9c-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bbf9c-119">L'indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d'adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de carnet d'adresses prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="bbf9c-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bbf9c-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bbf9c-121">Le fournisseur de carnet d'adresses ne fournit pas de modèles uniques.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbf9c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbf9c-122">Remarks</span></span>

<span data-ttu-id="bbf9c-123">MAPI appelle la méthode **GetOneOffTable** pour mettre à disposition des modèles uniques pour créer des destinataires.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="bbf9c-124">Les nouveaux destinataires sont ajoutés à la liste des destinataires d'un message sortant.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="bbf9c-125">Les fournisseurs de carnets d'adresses doivent prendre en charge la notification sur leur table ponctuelle pour informer MAPI des modifications de modèle.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="bbf9c-126">MAPI conserve la table ponctuelle ouverte pour activer la mise à jour dynamique.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="bbf9c-127">Les fournisseurs de carnets d'adresses peuvent également prendre en charge une table ponctuelle pour chacun de leurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="bbf9c-128">Les appelants extraient cette table ponctuelle en appelant la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur et en demandant la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bbf9c-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="bbf9c-129">Les modèles disponibles dans ce tableau permettent d'ajouter des destinataires au conteneur.</span><span class="sxs-lookup"><span data-stu-id="bbf9c-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="bbf9c-130">Pour plus d'informations sur les différences entre les deux types de tables ponctuelles, reportez-vous à la rubrique [implementIng One-Off tables](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bbf9c-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="bbf9c-131">Pour obtenir la liste des colonnes requises dans la table ponctuelle d'un fournisseur de carnet d'adresses, consultez la rubrique [tables One-Off](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bbf9c-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbf9c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbf9c-132">See also</span></span>



[<span data-ttu-id="bbf9c-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="bbf9c-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="bbf9c-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="bbf9c-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="bbf9c-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="bbf9c-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="bbf9c-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbf9c-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

