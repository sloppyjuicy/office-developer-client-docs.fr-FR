---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a15561a6f3af35c1c7c2285bb6252e6400e0e8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784374"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="80b7b-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="80b7b-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="80b7b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80b7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80b7b-105">Crée un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="80b7b-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="80b7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80b7b-106">Parameters</span></span>

 <span data-ttu-id="80b7b-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="80b7b-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="80b7b-108">[in] Pointeur vers le nom du nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="80b7b-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="80b7b-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="80b7b-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="80b7b-110">[in] Pointeur vers le mot de passe du nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="80b7b-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="80b7b-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="80b7b-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="80b7b-112">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="80b7b-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="80b7b-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80b7b-113">_ulFlags_</span></span>
  
> <span data-ttu-id="80b7b-114">[in] Masque de bits d’indicateurs qui contrôle la façon dont le profil est créé.</span><span class="sxs-lookup"><span data-stu-id="80b7b-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="80b7b-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="80b7b-115">The following flags can be set:</span></span>
    
<span data-ttu-id="80b7b-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="80b7b-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="80b7b-117">MAPI doit remplir le nouveau profil avec les services de message qui sont inclus dans la section [Services par défaut] du fichier Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="80b7b-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="80b7b-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="80b7b-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="80b7b-119">Vous pouvez afficher les feuilles de propriétés de configuration de chacun des fournisseurs dans les services de messagerie à ajouter.</span><span class="sxs-lookup"><span data-stu-id="80b7b-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="80b7b-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="80b7b-120">Return value</span></span>

<span data-ttu-id="80b7b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="80b7b-121">S_OK</span></span> 
  
> <span data-ttu-id="80b7b-122">Le nouveau profil a été créé.</span><span class="sxs-lookup"><span data-stu-id="80b7b-122">The new profile was created.</span></span>
    
<span data-ttu-id="80b7b-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="80b7b-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="80b7b-124">Le nouveau profil spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="80b7b-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80b7b-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="80b7b-125">Remarks</span></span>

<span data-ttu-id="80b7b-126">La méthode **IProfAdmin::CreateProfile** crée un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="80b7b-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="80b7b-127">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="80b7b-127">Notes to callers</span></span>

<span data-ttu-id="80b7b-128">Vous pouvez appeler **CreateProfile** au moment de l’installation ou à tout moment pendant une session.</span><span class="sxs-lookup"><span data-stu-id="80b7b-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="80b7b-129">Lorsque cette méthode est appelée au moment de l’installation, la plupart des paramètres de configuration proviennent de configuration du fichier Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="80b7b-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="80b7b-130">Lorsque cette méthode est appelée lors d’une session active, les paramètres proviennent de l’utilisateur est invité à travers une série de feuilles de propriétés.</span><span class="sxs-lookup"><span data-stu-id="80b7b-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="80b7b-131">Si l’indicateur MAPI_DEFAULT_SERVICES est défini dans le paramètre _ulFlags_ , **CreateProfile** appelle la fonction de point d’entrée de message service pour chaque service de message dans la section [Services par défaut] dans le fichier Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="80b7b-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="80b7b-132">Chaque fonction de point d’entrée de message service est appelée avec le paramètre _ulContext_ défini sur MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="80b7b-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="80b7b-133">Si indicateurs MAPI_DIALOG et de MAPI_DEFAULT_SERVICES sont définies, les valeurs dans les paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d’entrée de message service.</span><span class="sxs-lookup"><span data-stu-id="80b7b-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="80b7b-134">Les fonctions de point d’entrée de message service sont appelées uniquement une fois que toutes les informations disponibles à partir du fichier Mapisvc.inf a été ajoutées au profil.</span><span class="sxs-lookup"><span data-stu-id="80b7b-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="80b7b-135">Le nom du nouveau profil et son mot de passe peut être jusqu'à 64 caractères et peut inclure les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="80b7b-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="80b7b-136">Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement.</span><span class="sxs-lookup"><span data-stu-id="80b7b-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="80b7b-137">Des espaces, mais pas espaces à gauche ou.</span><span class="sxs-lookup"><span data-stu-id="80b7b-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="80b7b-138">Le paramètre _lpszPassword_ doit être NULL ou un pointeur vers une chaîne de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="80b7b-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80b7b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b7b-139">See also</span></span>



[<span data-ttu-id="80b7b-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="80b7b-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="80b7b-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="80b7b-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="80b7b-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="80b7b-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="80b7b-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80b7b-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

