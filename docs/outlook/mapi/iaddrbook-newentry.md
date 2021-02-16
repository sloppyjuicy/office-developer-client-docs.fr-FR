---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405099"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="3f613-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="3f613-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="3f613-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f613-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f613-105">Ajoute un nouveau destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="3f613-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="3f613-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f613-106">Parameters</span></span>

 <span data-ttu-id="3f613-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3f613-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="3f613-108">[in] Poignée vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3f613-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="3f613-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f613-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3f613-110">[in] Masque de bits d’indicateurs qui contrôle le type du texte utilisé.</span><span class="sxs-lookup"><span data-stu-id="3f613-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="3f613-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="3f613-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3f613-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f613-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3f613-113">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3f613-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="3f613-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="3f613-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3f613-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="3f613-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="3f613-116">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="3f613-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="3f613-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="3f613-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="3f613-118">[in] Pointeur vers l’identificateur d’entrée du conteneur où le nouveau destinataire doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="3f613-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="3f613-119">Si le paramètre  _cbEIDContainer_ est zéro, la méthode **NewEntry** renvoie un identificateur d’entrée de destinataire et une liste de modèles comme si la méthode [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) était appelée.</span><span class="sxs-lookup"><span data-stu-id="3f613-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="3f613-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="3f613-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="3f613-121">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEIDNewEntryTpl._</span><span class="sxs-lookup"><span data-stu-id="3f613-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="3f613-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="3f613-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="3f613-123">[in] Pointeur vers un modèle unique qui sera utilisé pour créer le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="3f613-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="3f613-124">Si  _cbEIDNewEntryTpl_ est zéro et  _lpEIDNewEntryTpl_ est NULL, **NewEntry** affiche une boîte de dialogue avec laquelle l’utilisateur peut choisir dans une liste de modèles pour l’ajout de nouvelles entrées.</span><span class="sxs-lookup"><span data-stu-id="3f613-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="3f613-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="3f613-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="3f613-126">[out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par _le paramètre lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="3f613-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="3f613-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="3f613-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="3f613-128">[out] Pointeur vers un pointeur vers l’identificateur d’entrée du nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="3f613-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f613-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f613-129">Return value</span></span>

<span data-ttu-id="3f613-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f613-130">S_OK</span></span> 
  
> <span data-ttu-id="3f613-131">La nouvelle entrée de carnet d’adresses a été créée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3f613-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f613-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f613-132">Remarks</span></span>

<span data-ttu-id="3f613-133">La **méthode NewEntry** crée une entrée de carnet d’adresses, à ajouter directement dans un conteneur ou à utiliser pour traiter un message sortant.</span><span class="sxs-lookup"><span data-stu-id="3f613-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3f613-134">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3f613-134">Notes to callers</span></span>

<span data-ttu-id="3f613-135">Si vous souhaitez que la nouvelle entrée soit ajoutée à un conteneur spécifique, définissez  _lpEIDContainer_ sur l’identificateur d’entrée du conteneur et  _cbEIDContainer_ sur le nombre d’byte dans l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3f613-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="3f613-136">Si vous souhaitez que la nouvelle entrée soit ajoutée à la liste des destinataires d’un message sortant, définissez  _lpEIDContainer_ sur NULL et  _cbEIDContainer_ sur zéro.</span><span class="sxs-lookup"><span data-stu-id="3f613-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="3f613-137">Si vous souhaitez autoriser l’utilisateur d’une application cliente à sélectionner le type d’entrée à créer, passez zéro dans  _cbEIDNewEntryTpl_ et NULL dans  _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="3f613-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="3f613-138">La **méthode NewEntry** affiche la table UNIQUE MAPI, une liste de modèles pris en charge par MAPI et par chaque fournisseur de carnet d’adresses dans la session.</span><span class="sxs-lookup"><span data-stu-id="3f613-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="3f613-139">Chaque modèle peut créer une entrée de destinataire pour un ou plusieurs types d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3f613-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="3f613-140">Si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée, passez des pointeurs valides dans les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="3f613-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="3f613-141">Vous devez libérer cet identificateur d’entrée lorsque vous en avez terminé en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="3f613-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="3f613-142">Pour utiliser un modèle particulier afin d’ajouter une nouvelle entrée à un conteneur modifiable, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="3f613-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="3f613-143">Appelez [la méthode IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre  _lpEntryID_ sur l’identificateur d’entrée du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3f613-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="3f613-144">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur de destination et définissez le paramètre  _ulPropTag_ sur **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre  _lpiid_ sur IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="3f613-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="3f613-145">Le conteneur retourne une table unique qui répertorie tous les modèles qu’il prend en charge pour la création de nouvelles entrées.</span><span class="sxs-lookup"><span data-stu-id="3f613-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="3f613-146">Récupérez la ligne qui représente le modèle pour le type particulier d’entrée que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="3f613-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="3f613-147">La **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d’adresse pris en charge par le modèle.</span><span class="sxs-lookup"><span data-stu-id="3f613-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="3f613-148">Appelez **la méthode NewEntry** et définissez  _lpEIDNewEntryTpl_ sur l’identificateur d’entrée du modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3f613-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="3f613-149">L’identificateur **d’entrée sera PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne du modèle dans le tableau unique.</span><span class="sxs-lookup"><span data-stu-id="3f613-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="3f613-150">Passez zéro dans  _cbEIDContainer_ et NULL dans  _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="3f613-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="3f613-151">Passez un pointeur valide dans le paramètre  _lppEIDNewEntry_ si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="3f613-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3f613-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f613-152">See also</span></span>



[<span data-ttu-id="3f613-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3f613-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="3f613-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="3f613-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="3f613-155">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="3f613-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="3f613-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3f613-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

