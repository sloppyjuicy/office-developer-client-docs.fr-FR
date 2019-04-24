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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341698"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="81230-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81230-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="81230-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81230-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81230-105">Établit le conteneur spécifié en tant que conteneur de carnet d'adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="81230-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="81230-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81230-106">Parameters</span></span>

 <span data-ttu-id="81230-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="81230-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="81230-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="81230-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="81230-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="81230-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="81230-110">dans Pointeur vers l'identificateur d'entrée du conteneur de carnet d'adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="81230-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81230-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81230-111">Return value</span></span>

<span data-ttu-id="81230-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="81230-112">S_OK</span></span> 
  
> <span data-ttu-id="81230-113">Le conteneur de carnet d'adresses par défaut a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="81230-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81230-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="81230-114">Remarks</span></span>

<span data-ttu-id="81230-115">Les clients et les fournisseurs de services appellent la méthode **SetDefaultDir** pour établir un nouveau conteneur de carnet d'adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="81230-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="81230-116">Le conteneur par défaut est le conteneur que l'utilisateur voit apparaître dans le carnet d'adresses lors de la première ouverture du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="81230-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="81230-117">**SetDefaultDir** enregistre le conteneur par défaut sous la forme d'une entrée dans le profil.</span><span class="sxs-lookup"><span data-stu-id="81230-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="81230-118">Le conteneur reste par défaut jusqu'à ce qu'un autre appel à **SetDefaultDir** soit effectué dans la même session ou dans une autre session, ou que le conteneur soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="81230-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="81230-119">La propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) correspond au paramètre **choisir automatiquement** dans la boîte de dialogue Options du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="81230-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="81230-120">Lorsque cette propriété existe dans la section de profil [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) et qu'elle est définie sur **true**, la boîte de dialogue Carnet d'adresses ne prend plus par défaut le conteneur spécifié par **SetDefaultDir**, mais choisit un carnet d'adresses que Microsoft Outlook considère comme indiqué. approprié pour le contexte dans lequel la boîte de dialogue s'affichait.</span><span class="sxs-lookup"><span data-stu-id="81230-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="81230-121">Notez que cela peut entraîner une mauvaise expérience des fournisseurs de carnets d'adresses tiers.</span><span class="sxs-lookup"><span data-stu-id="81230-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="81230-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="81230-122">MFCMAPI reference</span></span>

<span data-ttu-id="81230-123">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="81230-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="81230-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="81230-124">**File**</span></span>|<span data-ttu-id="81230-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="81230-125">**Function**</span></span>|<span data-ttu-id="81230-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="81230-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81230-127">Abcontdlg. cpp</span><span class="sxs-lookup"><span data-stu-id="81230-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="81230-128">CAbContDlg:: OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81230-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="81230-129">MFCMAPI utilise la méthode **SetDefaultDir** pour définir le conteneur de carnet d'adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="81230-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81230-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81230-130">See also</span></span>



[<span data-ttu-id="81230-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81230-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="81230-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="81230-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="81230-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="81230-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="81230-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="81230-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="81230-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="81230-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="81230-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="81230-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

