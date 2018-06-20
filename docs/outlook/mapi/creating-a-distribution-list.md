---
title: Création d’une liste de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 82fa28f021dbb839c7bb05974682f0bb24174bb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783098"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="63912-103">Création d’une liste de distribution</span><span class="sxs-lookup"><span data-stu-id="63912-103">Creating a distribution list</span></span>

<span data-ttu-id="63912-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63912-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63912-105">Les clients peuvent créer une liste de distribution directement dans un conteneur modifiable telles que le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="63912-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="63912-106">**Pour créer une liste de distribution dans le carnet d’adresses personnel**</span><span class="sxs-lookup"><span data-stu-id="63912-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="63912-107">Créez un tableau de balise de propriété ajustés avec la balise d’une propriété, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), comme suit :</span><span class="sxs-lookup"><span data-stu-id="63912-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="63912-108">Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="63912-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="63912-109">Si une erreur se produit ou **GetPAB** renvoie zéro ou NULL, ne continuez pas.</span><span class="sxs-lookup"><span data-stu-id="63912-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="63912-110">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="63912-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="63912-111">Le paramètre de sortie _ulObjType_ doit être défini sur MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="63912-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="63912-112">Appeler [IMAPIProp::GetProps](imapiprop-getprops.md) méthode le carnet d’adresses du personnel pour récupérer la propriété PR_DEF_CREATE_DL, le modèle utilisé pour créer une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="63912-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="63912-113">En cas d’échec de **GetProps** :</span><span class="sxs-lookup"><span data-stu-id="63912-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="63912-114">Appelez le carnet d’adresses du personnel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="63912-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="63912-115">Créer une restriction de propriété pour rechercher la ligne contenant la colonne **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) égale à « MAPIPDL ».</span><span class="sxs-lookup"><span data-stu-id="63912-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="63912-116">Appel [IMAPITable::FindRow](imapitable-findrow.md) pour rechercher cette ligne.</span><span class="sxs-lookup"><span data-stu-id="63912-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="63912-117">Enregistrez l’identificateur d’entrée renvoyée par **GetProps** ou **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="63912-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="63912-118">Appelez le carnet d’adresses du personnel [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer une nouvelle entrée à l’aide du modèle représenté par l’identificateur d’entrée enregistrée.</span><span class="sxs-lookup"><span data-stu-id="63912-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="63912-119">Ne pensez pas que l’objet retourné sera une liste de distribution plutôt que d’un utilisateur de messagerie lorsque cet appel est distant.</span><span class="sxs-lookup"><span data-stu-id="63912-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="63912-120">Notez que l’indicateur CREATE_CHECK_DUP est passé dans le paramètre _ulFlags_ pour empêcher que l’entrée ajoutée à deux reprises.</span><span class="sxs-lookup"><span data-stu-id="63912-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="63912-121">Appeler la méthode **IUnknown::QueryInterface** de la nouvelle entrée, en passant IID_IDistList comme l’identificateur d’interface pour déterminer si l’entrée est une liste de distribution et prend en charge la [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span><span class="sxs-lookup"><span data-stu-id="63912-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="63912-122">**CreateEntry** renvoie un pointeur **IMAPIProp** plutôt que le pointeur **IMailUser** ou **IDistList** plus spécifique, vérifiez que l’objet d’une liste de distribution a été créé.</span><span class="sxs-lookup"><span data-stu-id="63912-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="63912-123">Si **QueryInterface** réussit, vous pouvez être sûr que vous avez créé une liste de distribution plutôt que d’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="63912-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="63912-124">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la liste de distribution pour définir son nom d’affichage et d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="63912-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="63912-125">Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de la liste de distribution pour ajouter un ou plusieurs utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="63912-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="63912-126">Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la liste de distribution lorsque vous êtes prêt à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="63912-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="63912-127">Pour récupérer l’identificateur d’entrée de la liste de distribution enregistrée, définir l’indicateur KEEP_OPEN_READWRITE, puis appelez [IMAPIProp::GetProps](imapiprop-getprops.md) demande la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63912-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="63912-128">Publier la nouvelle liste de distribution et le carnet d’adresses personnel en appelant leurs méthodes **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="63912-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="63912-129">Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour l’identificateur d’entrée du carnet d’adresses personnel et le tableau de balise de propriété ajustés.</span><span class="sxs-lookup"><span data-stu-id="63912-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

