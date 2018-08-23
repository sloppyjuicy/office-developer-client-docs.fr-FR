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
ms.openlocfilehash: eaf472a380acd62cddb2c20c35335ccb1e2ce07f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585856"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="ec4ae-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="ec4ae-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="ec4ae-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec4ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec4ae-105">Ajoute un destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ec4ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec4ae-106">Parameters</span></span>

 <span data-ttu-id="ec4ae-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ec4ae-108">[in] Handle vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="ec4ae-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ec4ae-110">[in] Masque de bits d’indicateurs qui contrôle le type du texte qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="ec4ae-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="ec4ae-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ec4ae-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ec4ae-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ec4ae-113">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ec4ae-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ec4ae-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="ec4ae-116">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="ec4ae-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="ec4ae-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="ec4ae-118">[in] Pointeur vers l’identificateur d’entrée du conteneur dans lequel le nouveau destinataire doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="ec4ae-119">Si le paramètre _cbEIDContainer_ est égale à zéro, la méthode **NewEntry** renvoie un identificateur d’entrée du destinataire et une liste de modèles comme si la méthode [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="ec4ae-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="ec4ae-121">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEIDNewEntryTpl_ .</span><span class="sxs-lookup"><span data-stu-id="ec4ae-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="ec4ae-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="ec4ae-123">[in] Pointeur vers un modèle unique qui sera utilisé pour créer le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="ec4ae-124">Si _cbEIDNewEntryTpl_ est égale à zéro et _lpEIDNewEntryTpl_ est NULL, **NewEntry** affiche une boîte de dialogue avec laquelle l’utilisateur peut sélectionner dans une liste de modèles pour l’ajout de nouvelles entrées.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="ec4ae-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="ec4ae-126">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="ec4ae-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="ec4ae-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="ec4ae-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="ec4ae-128">[out] Pointeur vers un pointeur vers l’identificateur d’entrée du nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec4ae-129">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ec4ae-129">Return value</span></span>

<span data-ttu-id="ec4ae-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec4ae-130">S_OK</span></span> 
  
> <span data-ttu-id="ec4ae-131">La nouvelle entrée de carnet d’adresses a été créée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec4ae-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec4ae-132">Remarks</span></span>

<span data-ttu-id="ec4ae-133">La méthode **NewEntry** crée une nouvelle adresse entrée de l’annuaire à ajouter directement dans un conteneur ou à utiliser pour envoyer un message sortant.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ec4ae-134">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ec4ae-134">Notes to callers</span></span>

<span data-ttu-id="ec4ae-135">Si vous souhaitez que la nouvelle entrée à ajouter à un conteneur spécifique, la valeur _lpEIDContainer_ identificateur d’entrée et de _cbEIDContainer_ pour le nombre d’octets dans l’identificateur d’entrée du conteneur.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="ec4ae-136">Si vous souhaitez que la nouvelle entrée à ajouter à la liste des destinataires d’un message sortant, la valeur _lpEIDContainer_ NULL et _cbEIDContainer_ à zéro.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="ec4ae-137">Si vous souhaitez permettre à l’utilisateur d’une application cliente pour sélectionner le type d’entrée à créer, passez zéro dans _cbEIDNewEntryTpl_ et NULL dans _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="ec4ae-138">La méthode **NewEntry** affiche la table unique MAPI, une liste de modèles pris en charge par MAPI et par chaque fournisseur de carnet d’adresses dans la session.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="ec4ae-139">Chaque modèle peut créer une entrée pour un ou plusieurs types d’adresse du destinataire.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="ec4ae-140">Si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée, passez les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry_ pointeurs valides.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="ec4ae-141">Vous êtes responsable de libérer de l’identificateur d’entrée lorsque vous avez terminé de l’utiliser en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec4ae-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="ec4ae-142">Pour utiliser un modèle particulier pour ajouter une nouvelle entrée à un conteneur modifiable, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="ec4ae-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="ec4ae-143">Appelez la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre _lpEntryID_ à l’identificateur d’entrée du conteneur.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="ec4ae-144">Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) méthode du conteneur destination et définissez le paramètre _ulPropTag_ **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre _lpiid_ sur IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="ec4ae-145">Le conteneur renvoie un tableau unique qui répertorie tous les modèles pris en charge pour la création de nouvelles entrées.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="ec4ae-146">Récupérer la ligne qui représente le modèle pour le type particulier d’entrée que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="ec4ae-147">La colonne **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d’adresse est pris en charge par le modèle.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="ec4ae-148">Appelez la méthode **NewEntry** et définissez _lpEIDNewEntryTpl_ sur l’identificateur d’entrée du modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="ec4ae-149">L’identificateur d’entrée sera la colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne du modèle dans la table unique.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="ec4ae-150">Passez zéro dans _cbEIDContainer_ et NULL dans _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="ec4ae-151">Passez un pointeur valid dans le paramètre _lppEIDNewEntry_ si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ec4ae-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec4ae-152">See also</span></span>



[<span data-ttu-id="ec4ae-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ec4ae-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="ec4ae-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="ec4ae-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="ec4ae-155">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="ec4ae-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="ec4ae-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ec4ae-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

