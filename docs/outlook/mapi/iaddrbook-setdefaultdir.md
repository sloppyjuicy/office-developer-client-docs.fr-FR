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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341698"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="ca0d5-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ca0d5-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="ca0d5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca0d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca0d5-105">Établit le conteneur spécifié en tant que conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ca0d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca0d5-106">Parameters</span></span>

 <span data-ttu-id="ca0d5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca0d5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ca0d5-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ca0d5-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ca0d5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca0d5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ca0d5-110">[in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca0d5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca0d5-111">Return value</span></span>

<span data-ttu-id="ca0d5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca0d5-112">S_OK</span></span> 
  
> <span data-ttu-id="ca0d5-113">Le conteneur de carnet d’adresses par défaut a été correctement définie.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca0d5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca0d5-114">Remarks</span></span>

<span data-ttu-id="ca0d5-115">Les clients et les fournisseurs de services appellent la **méthode SetDefaultDir** pour établir un nouveau conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="ca0d5-116">Le conteneur par défaut est celui que l’utilisateur voit s’afficher dans le carnet d’adresses lors de sa première ouverture.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="ca0d5-117">**SetDefaultDir enregistre** le conteneur par défaut en tant qu’entrée dans le profil.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="ca0d5-118">Le conteneur reste le conteneur par défaut jusqu’à ce qu’un autre appel à **SetDefaultDir** soit effectué dans la même session ou dans une autre session, ou que le conteneur soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ca0d5-119">La [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) correspond au paramètre **Choisir** automatiquement dans la boîte de dialogue Options du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="ca0d5-120">Lorsque cette propriété existe dans la section profil [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) et est définie sur **true**, la boîte de dialogue carnet d’adresses n’est plus définie par défaut sur le conteneur spécifié par **SetDefaultDir**, mais choisit un carnet d’adresses que Microsoft Outlook considère approprié pour le contexte dans lequel la boîte de dialogue a été affichée.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="ca0d5-121">Notez que cela peut entraîner une expérience médiocre pour les fournisseurs de carnets d’adresses tiers.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ca0d5-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ca0d5-122">MFCMAPI reference</span></span>

<span data-ttu-id="ca0d5-123">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ca0d5-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ca0d5-124">**File**</span></span>|<span data-ttu-id="ca0d5-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ca0d5-125">**Function**</span></span>|<span data-ttu-id="ca0d5-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ca0d5-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca0d5-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ca0d5-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="ca0d5-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ca0d5-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="ca0d5-129">MFCMAPI utilise la **méthode SetDefaultDir** pour définir le conteneur de carnet d’adresses spécifié comme conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca0d5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca0d5-130">See also</span></span>



[<span data-ttu-id="ca0d5-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ca0d5-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="ca0d5-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ca0d5-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="ca0d5-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="ca0d5-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="ca0d5-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ca0d5-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="ca0d5-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ca0d5-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ca0d5-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ca0d5-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

