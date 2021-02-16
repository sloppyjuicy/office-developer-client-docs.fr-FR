---
title: Mise en œuvre de l’logo et de la ffage du fournisseur de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438735"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="a6b6d-103">Mise en œuvre de l’logo et de la ffage du fournisseur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="a6b6d-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="a6b6d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6b6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6b6d-105">Les fournisseurs de carnets d’adresses peuvent prendre en charge l’ouverture de session et la vidage de session en implémentant les méthodes de l’interface [IABProvider : IUnknown.](iabprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a6b6d-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="a6b6d-106">L’interface \*\* IABProvider \*\* hérite directement **d’IUnknown** et n’ajoute que deux autres méthodes : **Logon** et **Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="a6b6d-107">Déconnexion</span><span class="sxs-lookup"><span data-stu-id="a6b6d-107">Logoff</span></span>

<span data-ttu-id="a6b6d-108">MAPI appelle la méthode [IABProvider::Logon](iabprovider-logon.md) de votre fournisseur au début de chaque session et chaque fois que votre fournisseur est ajouté au profil actuel et que le client prend en charge la reconfiguration dynamique.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="a6b6d-109">Lorsque MAPI appelle **la méthode IABProvider::Logon,** votre fournisseur de carnet d’adresses commence son processus d’accès.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="a6b6d-110">**Pour implémenter IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="a6b6d-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="a6b6d-111">Initialiser tous les pointeurs de paramètre de sortie transmis par MAPI.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="a6b6d-112">Appelez la méthode **IUnknown::AddRef** de l’objet de support pour incrémenter son nombre de références.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="a6b6d-113">Appelez la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de support pour ouvrir la section du profil qui contient des informations de configuration sur votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="a6b6d-114">Passez null pour le  _paramètre lpUID_ et l’MAPI_MODIFY si vous avez l’intention d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="a6b6d-115">Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la section de profil pour récupérer les propriétés dont votre fournisseur a besoin pour l’accès, telles que le nom du fichier de données ou de la table de base de données.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="a6b6d-116">Vérifiez que les propriétés sont toutes disponibles et valides.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="a6b6d-117">Si nécessaire et autorisé, affichez une boîte de dialogue pour demander à l’utilisateur d’apporter des corrections ou des ajouts à des informations non valides ou manquantes et appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section de profil pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="a6b6d-118">Voici quelques-unes des propriétés courantes qui doivent être disponibles :</span><span class="sxs-lookup"><span data-stu-id="a6b6d-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="a6b6d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6b6d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="a6b6d-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6b6d-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="a6b6d-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6b6d-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="a6b6d-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6b6d-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="a6b6d-123">Ne définissez **pas PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6b6d-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="a6b6d-124">Au moment de l’logo, ces propriétés sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="a6b6d-125">Si une ou plusieurs propriétés de configuration ne sont pas disponibles, échouez et renvoyez la valeur MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="a6b6d-126">Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire [un MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="a6b6d-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="a6b6d-127">Votre fournisseur peut créer un **MAPIUID** en :</span><span class="sxs-lookup"><span data-stu-id="a6b6d-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="a6b6d-128">Appel de [la méthode IMAPISupport::NewUID.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="a6b6d-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="a6b6d-129">Appel de lUUIDGEN.EXE pour définir un GUID que votre fournisseur utilise pour inclure dans l’un de ses fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="a6b6d-130">Si vous le souhaitez, enregistrez un **MAPIUID** nouvellement créé dans le profil actuel en appelant la méthode \*\* IMAPIProp::SetProps \*\* de la section de profil.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="a6b6d-131">Publiez la section profil en appelant **sa méthode IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="a6b6d-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="a6b6d-132">Ins instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="a6b6d-133">Étant donné qu’il est possible pour MAPI d’appeler votre méthode \*\* Logon \*\* plusieurs fois au cours d’une session, il est judicieux de prendre en charge cette possibilité dans votre implémentation en étant en mesure de créer plusieurs objets d’ouverture de session et de suivre chaque objet créé.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="a6b6d-134">La prise **en** charge de plusieurs appels d’ouverture de session permet à un utilisateur d’une application cliente, par exemple, de se connecter à une session avec différentes identités ou d’utiliser des destinations de remise différentes.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="a6b6d-135">**L’arrêt** est appelé à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="a6b6d-136">MAPI appelle votre [méthode IABProvider::Shutdown](iabprovider-shutdown.md) comme l’une des dernières tâches impliquées dans l’arrêt d’une session.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="a6b6d-137">MAPI a libéré tous les objets d’accès de votre fournisseur et, lorsque celui-ci reçoit cet appel, il peut supposer qu’il s’agit du dernier appel qu’il recevra.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="a6b6d-138">Dans votre implémentation de **IABProvider::Shutdown,** effectuez tout nettoyage final que vous pensez nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="a6b6d-139">Par exemple, votre fournisseur peut appeler **MAPIDeinitIdle** s’il a appelé **MAPIInitIdle** pour utiliser le moteur inactif pendant la session ou la méthode **IUnknown::Release** des objets qui n’ont pas encore été publiés.</span><span class="sxs-lookup"><span data-stu-id="a6b6d-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="a6b6d-140">Si votre fournisseur n’a pas de nettoyage final, son implémentation peut être composé d’une seule ligne de code :</span><span class="sxs-lookup"><span data-stu-id="a6b6d-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


