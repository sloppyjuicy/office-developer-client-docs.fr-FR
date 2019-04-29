---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423859"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="73869-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="73869-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="73869-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73869-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73869-105">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="73869-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="73869-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73869-106">Parameters</span></span>

<span data-ttu-id="73869-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73869-107">_ulFlags_</span></span>
  
> <span data-ttu-id="73869-108">dans Masque de des indicateurs qui contrôle le type du texte dans les chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="73869-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="73869-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="73869-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="73869-110">MAPI_CACHE_ONLY: Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="73869-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="73869-111">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="73869-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="73869-112">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="73869-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="73869-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="73869-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="73869-114">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés qui nécessitent une mise à jour, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="73869-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="73869-115">Le paramètre _lpPropTagArray_ peut être null.</span><span class="sxs-lookup"><span data-stu-id="73869-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="73869-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="73869-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="73869-117">dans Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="73869-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="73869-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="73869-118">Return value</span></span>

<span data-ttu-id="73869-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="73869-119">S_OK</span></span> 
  
> <span data-ttu-id="73869-120">La liste des destinataires a été préparée.</span><span class="sxs-lookup"><span data-stu-id="73869-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="73869-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="73869-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="73869-122">Au moins un des destinataires dans le paramètre _lpRecipList_ n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="73869-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="73869-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="73869-123">Return value</span></span>

<span data-ttu-id="73869-124">Un client appelle la méthode MAPI [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) pour modifier ou réorganiser un ensemble de propriétés pour un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="73869-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="73869-125">Les destinataires peuvent ou non faire partie de la liste des destinataires d'un message sortant.</span><span class="sxs-lookup"><span data-stu-id="73869-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="73869-126">MAPI transfère cet appel à la méthode IABLogon du fournisseur de carnet d'adresses **::P reparerecips** .</span><span class="sxs-lookup"><span data-stu-id="73869-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="73869-127">**IABLogon::P reparerecips** effectue quatre tâches principales:</span><span class="sxs-lookup"><span data-stu-id="73869-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="73869-128">Garantit que tous les destinataires de la liste d'adresses vers laquelle pointe le paramètre _lpRecipList_ ont un identificateur d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="73869-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="73869-129">Garantit que tous les destinataires ont les propriétés spécifiées dans le tableau de valeurs de propriété vers lequel pointe le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="73869-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="73869-130">Garantit que les propriétés du tableau de valeurs de propriété apparaissent avant les autres propriétés qui existaient avant l'appel.</span><span class="sxs-lookup"><span data-stu-id="73869-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="73869-131">Garantit que l'ordre des propriétés dans la structure [ADRENTRY](adrentry.md) de chaque destinataire dans la structure **ADRLIST** est le même que dans le tableau de valeurs de la propriété.</span><span class="sxs-lookup"><span data-stu-id="73869-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="73869-132">La structure **ADRENTRY** dans le paramètre _lpRecipList_ contient une structure **ADRENTRY** pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="73869-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="73869-133">Chaque structure **ADRENTRY** contient un tableau de structures [SPropValue](spropvalue.md) pour décrire les propriétés du destinataire.</span><span class="sxs-lookup"><span data-stu-id="73869-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="73869-134">Lorsque **IABLogon::P reparerecips** renvoie, le tableau de structures **SPropValue** pour chaque destinataire inclut les propriétés de l' _lpPropTagArray_ suivies par les autres propriétés du destinataire.</span><span class="sxs-lookup"><span data-stu-id="73869-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73869-135">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="73869-135">Notes to implementers</span></span>

<span data-ttu-id="73869-136">Implémentation de **IABLogon::P reparerecips** implique de placer des propriétés dans un ordre spécifique, d'extraire des valeurs de propriétés et de convertir des identificateurs d'entrée à court terme en identificateurs d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="73869-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="73869-137">Les propriétés qui sont demandées dans le paramètre _lpPropTagArray_ doivent se trouver au début du tableau de valeurs de la propriété associé à la structure **ADRENTRY** de chaque destinataire dans le paramètre _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="73869-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="73869-138">Si les valeurs de ces propriétés n'existent pas, ouvrez l'utilisateur de messagerie associé ou la liste de distribution à l'aide de son identificateur d'entrée et récupérez les valeurs de propriété manquantes.</span><span class="sxs-lookup"><span data-stu-id="73869-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="73869-139">AlLouez chaque structure **SPropValue** passée dans _lpRecipList_ séparément afin que les structures puissent être libérées individuellement.</span><span class="sxs-lookup"><span data-stu-id="73869-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="73869-140">Si vous devez allouer de l'espace supplémentaire pour une structure **SPropValue** , par exemple, pour stocker les données d'une propriété de type chaîne, utilisez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer de l'espace supplémentaire pour le tableau de valeurs de la propriété complète.</span><span class="sxs-lookup"><span data-stu-id="73869-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="73869-141">Utilisez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de valeurs de propriété d'origine, puis utilisez la fonction [MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire requise.</span><span class="sxs-lookup"><span data-stu-id="73869-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="73869-142">Pour implémenter **IABLogon::P reparerecips**, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="73869-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="73869-143">Vérifiez les entrées dans le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="73869-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="73869-144">Si le tableau de valeurs de la propriété est vide, il n'y a aucun travail à faire.</span><span class="sxs-lookup"><span data-stu-id="73869-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="73869-145">Renvoyer une valeur de réussite.</span><span class="sxs-lookup"><span data-stu-id="73869-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="73869-146">Traitez chaque destinataire dans le paramètre _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="73869-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="73869-147">Il existe un membre de structure **ADRENTRY** pour chaque destinataire dans la liste.</span><span class="sxs-lookup"><span data-stu-id="73869-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="73869-148">Ignorez les types de destinataires suivants:</span><span class="sxs-lookup"><span data-stu-id="73869-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="73869-149">Destinataires sans identificateur d'entrée dans le membre **rgPropVals** de leur structure **ADRENTRY** (c'est-à-dire, destinataires non résolus).</span><span class="sxs-lookup"><span data-stu-id="73869-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="73869-150">Les destinataires dont l'identificateur d'entrée n'appartient pas à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="73869-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="73869-151">Ces destinataires seront transmis à un autre fournisseur de carnets d'adresses.</span><span class="sxs-lookup"><span data-stu-id="73869-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="73869-152">Ouvrez le destinataire et extrayez les propriétés qui sont déjà définies pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="73869-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="73869-153">Fusionnez le tableau de valeurs de propriété spécifié dans _lpRecipList_ avec le tableau de propriétés renvoyées à partir de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="73869-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="73869-154">Si la même propriété se produit dans les deux tableaux de propriétés, utilisez la valeur de _lpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="73869-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="73869-155">Si le tableau de valeurs de la propriété _lpRecipList_ est suffisamment grand pour contenir toutes les propriétés nécessaires, il suffit de le remplacer par le tableau fusionné.</span><span class="sxs-lookup"><span data-stu-id="73869-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="73869-156">Si le tableau de valeurs de la propriété _lpRecipList_ n'est pas assez grand, remplacez-le par un tableau nouvellement alloué.</span><span class="sxs-lookup"><span data-stu-id="73869-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="73869-157">Assurez-vous que le nouveau tableau dispose d'une valeur mise à jour dans chacun de ses membres **cValues** .</span><span class="sxs-lookup"><span data-stu-id="73869-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="73869-158">Si vous ne connaissez pas une ou plusieurs des propriétés du paramètre _lpPropTagArray_ , définissez le type de la propriété dans la structure **ADRENTRY** du destinataire sur PT_ERROR et la valeur de la propriété sur MAPI_E_NOT_FOUND ou sur une autre valeur qui donne plus raison spécifique de l'indisponibilité de la propriété.</span><span class="sxs-lookup"><span data-stu-id="73869-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="73869-159">Pour plus d'informations sur PT_ERROR, consultez la rubrique [types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="73869-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="73869-160">Ne réaffectez jamais la structure **ADRLIST** passée dans **IABLogon::P reparerecips** ou modifier son nombre d'entrées.</span><span class="sxs-lookup"><span data-stu-id="73869-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73869-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73869-161">See also</span></span>

- [<span data-ttu-id="73869-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="73869-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="73869-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="73869-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="73869-164">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="73869-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="73869-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="73869-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="73869-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73869-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

