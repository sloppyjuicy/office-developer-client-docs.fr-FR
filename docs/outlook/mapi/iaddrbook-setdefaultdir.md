---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392710"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="439b7-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="439b7-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="439b7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="439b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="439b7-105">Définit le conteneur spécifié par le conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="439b7-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="439b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="439b7-106">Parameters</span></span>

 <span data-ttu-id="439b7-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="439b7-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="439b7-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="439b7-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="439b7-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="439b7-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="439b7-110">[in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="439b7-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="439b7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="439b7-111">Return value</span></span>

<span data-ttu-id="439b7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="439b7-112">S_OK</span></span> 
  
> <span data-ttu-id="439b7-113">Le conteneur de carnet d’adresses par défaut a été défini.</span><span class="sxs-lookup"><span data-stu-id="439b7-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="439b7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="439b7-114">Remarks</span></span>

<span data-ttu-id="439b7-115">Clients et fournisseurs de services appellent la méthode de **SetDefaultDir** pour établir un conteneur de carnet d’adresses par défaut nouveau.</span><span class="sxs-lookup"><span data-stu-id="439b7-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="439b7-116">Le conteneur par défaut est le conteneur dans lequel l’utilisateur voit affiché dans le carnet d’adresses lors de la première ouverture du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="439b7-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="439b7-117">**SetDefaultDir** enregistre le conteneur par défaut comme une entrée dans le profil.</span><span class="sxs-lookup"><span data-stu-id="439b7-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="439b7-118">Le conteneur reste en tant que la valeur par défaut jusqu'à ce qu’un autre appel à **SetDefaultDir** est effectué dans la même session ou dans une autre session, soit le conteneur est supprimé.</span><span class="sxs-lookup"><span data-stu-id="439b7-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="439b7-119">La propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) correspond au paramètre **d’Accepter automatiquement** dans la boîte de dialogue Options de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="439b7-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="439b7-120">Lorsque cette propriété existe dans la section profil [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) et est définie sur **true**, la boîte de dialogue Carnet d’adresses n’est plus le conteneur spécifié par **SetDefaultDir**par défaut, mais choisit un carnet d’adresses qui prend en compte Microsoft Outlook approprié pour le contexte dans lequel la boîte de dialogue a été affiché.</span><span class="sxs-lookup"><span data-stu-id="439b7-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="439b7-121">Notez que cela peut entraîner une mauvaise expérience pour les fournisseurs de carnet d’adresses tiers.</span><span class="sxs-lookup"><span data-stu-id="439b7-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="439b7-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="439b7-122">MFCMAPI reference</span></span>

<span data-ttu-id="439b7-123">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="439b7-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="439b7-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="439b7-124">**File**</span></span>|<span data-ttu-id="439b7-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="439b7-125">**Function**</span></span>|<span data-ttu-id="439b7-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="439b7-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="439b7-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="439b7-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="439b7-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="439b7-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="439b7-129">MFCMAPI utilise la méthode **SetDefaultDir** pour effectuer le conteneur de carnet d’adresse spécifiée par défaut.</span><span class="sxs-lookup"><span data-stu-id="439b7-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="439b7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="439b7-130">See also</span></span>



[<span data-ttu-id="439b7-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="439b7-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="439b7-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="439b7-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="439b7-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="439b7-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="439b7-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="439b7-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="439b7-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="439b7-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="439b7-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="439b7-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

