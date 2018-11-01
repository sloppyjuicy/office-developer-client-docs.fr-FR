---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593472"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="9219b-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="9219b-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="9219b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9219b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9219b-105">Enregistre une description d’un formulaire particulier dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9219b-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="9219b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9219b-106">Parameters</span></span>

 <span data-ttu-id="9219b-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="9219b-107">_szFileName_</span></span>
  
> <span data-ttu-id="9219b-108">[in] Chaîne qui nomme le fichier de message de description du formulaire où sa description est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="9219b-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="9219b-109">Ce nom de fichier doit avoir l’extension .fdm.</span><span class="sxs-lookup"><span data-stu-id="9219b-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9219b-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9219b-110">Return value</span></span>

<span data-ttu-id="9219b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9219b-111">S_OK</span></span> 
  
> <span data-ttu-id="9219b-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="9219b-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9219b-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="9219b-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="9219b-114">Le fichier de configuration n’a pas pu être écrites.</span><span class="sxs-lookup"><span data-stu-id="9219b-114">The configuration file could not be written.</span></span> <span data-ttu-id="9219b-115">Pour obtenir la structure [MAPIERROR](mapierror.md) qui est associée à l’erreur, appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9219b-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="9219b-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9219b-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9219b-117">**SaveForm** a été appelée probablement pour enregistrer un formulaire dans le conteneur de formulaire local.</span><span class="sxs-lookup"><span data-stu-id="9219b-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="9219b-118">**SaveForm** n’est pas pris en charge sur le conteneur de formulaire local.</span><span class="sxs-lookup"><span data-stu-id="9219b-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9219b-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="9219b-119">Remarks</span></span>

<span data-ttu-id="9219b-120">Applications clientes appellent la méthode **IMAPIFormInfo::SaveForm** pour enregistrer une description du formulaire actif dans le fichier portant le nom de fichier donné.</span><span class="sxs-lookup"><span data-stu-id="9219b-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="9219b-121">**SaveForm** crée un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9219b-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9219b-122">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="9219b-122">Notes to callers</span></span>

<span data-ttu-id="9219b-123">Vous pouvez réinstaller les formulaires en les sélectionnant à partir d’une liste de formulaire descripteur messages dans une boîte de dialogue Affichage de fournisseurs de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="9219b-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="9219b-124">L’extension recommandée pour les messages de descripteur de formulaire est .fdm.</span><span class="sxs-lookup"><span data-stu-id="9219b-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="9219b-125">Appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) si **SaveForm** renvoie MAPI_E_EXTENDED_ERROR et vérifiez la structure **MAPIERROR** retournée pour déterminer la condition qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9219b-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9219b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9219b-126">See also</span></span>



[<span data-ttu-id="9219b-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9219b-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="9219b-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="9219b-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="9219b-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9219b-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

