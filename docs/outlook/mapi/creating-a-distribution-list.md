---
title: Création d’une liste de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424174"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="fc9d9-103">Création d’une liste de distribution</span><span class="sxs-lookup"><span data-stu-id="fc9d9-103">Creating a distribution list</span></span>

<span data-ttu-id="fc9d9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc9d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc9d9-105">Les clients peuvent créer une liste de distribution directement dans un conteneur modifiable tel que le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="fc9d9-106">**Pour créer une liste de distribution dans le PAB**</span><span class="sxs-lookup"><span data-stu-id="fc9d9-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="fc9d9-107">Créez un tableau de balises de propriétés de taille moyenne avec **une balise de PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), comme suit :</span><span class="sxs-lookup"><span data-stu-id="fc9d9-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="fc9d9-108">Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’identité.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="fc9d9-109">En cas d’erreur ou **si GetPAB** renvoie zéro ou NULL, ne continuez pas.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="fc9d9-110">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir le carnet d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="fc9d9-111">Le paramètre de sortie  _ulObjType_ doit être MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="fc9d9-112">Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du PAB pour récupérer la propriété PR_DEF_CREATE_DL, le modèle qu’il utilise pour créer une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="fc9d9-113">Si **GetProps échoue** :</span><span class="sxs-lookup"><span data-stu-id="fc9d9-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="fc9d9-114">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du PAB pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="fc9d9-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="fc9d9-115">Créez une restriction de propriété pour rechercher la ligne avec la **colonne PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) égale à « MAPIPDL ».</span><span class="sxs-lookup"><span data-stu-id="fc9d9-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="fc9d9-116">Appelez [IMAPITable::FindRow](imapitable-findrow.md) pour localiser cette ligne.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="fc9d9-117">Enregistrez l’identificateur d’entrée renvoyé **par GetProps** ou **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="fc9d9-118">Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) du PAB pour créer une entrée à l’aide du modèle représenté par l’identificateur d’entrée enregistré.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="fc9d9-119">Ne supposez pas que l’objet renvoyé sera une liste de distribution plutôt qu’un utilisateur de messagerie lorsque cet appel sera distant.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="fc9d9-120">Notez que l CREATE_CHECK_DUP est transmis dans le  _paramètre ulFlags_ pour empêcher l’ajout de l’entrée deux fois.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="fc9d9-121">Appelez la méthode **IUnknown::QueryInterface** de la nouvelle entrée, en passant IID_IDistList comme identificateur d’interface, pour déterminer si l’entrée est une liste de distribution et prend en charge l’interface [IDistList : IMAPIContainer.](idistlistimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="fc9d9-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="fc9d9-122">Étant **donné que CreateEntry** renvoie un pointeur **IMAPIProp** plutôt que le pointeur **IMailUser** ou **IDistList** plus spécifique, vérifiez qu’un objet de liste de distribution a été créé.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="fc9d9-123">Si **QueryInterface réussit,** vous pouvez être sûr d’avoir créé une liste de distribution plutôt qu’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="fc9d9-124">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la liste de distribution pour définir son nom complet et d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="fc9d9-125">Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de la liste de distribution pour ajouter un ou plusieurs utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="fc9d9-126">Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la liste de distribution lorsque vous êtes prêt à l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="fc9d9-127">Pour récupérer l’identificateur d’entrée de la liste de distribution enregistrée, définissez l’indicateur KEEP_OPEN_READWRITE, puis appelez [IMAPIProp::GetProps](imapiprop-getprops.md) demandant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fc9d9-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="fc9d9-128">Publiez la nouvelle liste de distribution et le PAB en appelant leurs **méthodes IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="fc9d9-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="fc9d9-129">Appelez [MAPIFreeBuffer pour](mapifreebuffer.md) libérer la mémoire de l’identificateur d’entrée du PAB et du tableau de balises de propriétés de taille.</span><span class="sxs-lookup"><span data-stu-id="fc9d9-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

