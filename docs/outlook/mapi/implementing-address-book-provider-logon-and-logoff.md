---
title: Implémentation d’ouverture et de fermeture de session de fournisseur de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f26e7b7ec607c9714012870d5367a0e775c62f34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572101"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="3e070-103">Implémentation d’ouverture et de fermeture de session de fournisseur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="3e070-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="3e070-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e070-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e070-105">Fournisseurs de carnet d’adresses en charge d’ouverture de session et de fermeture de session en implémentant les méthodes de le [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="3e070-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="3e070-106">Le ** IABProvider ** interface hérite directement à partir de **IUnknown** et ajoute deux autres méthodes : **ouverture de session** et **d’arrêt**.</span><span class="sxs-lookup"><span data-stu-id="3e070-106">The ** IABProvider ** interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="3e070-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="3e070-107">Logoff</span></span>

<span data-ttu-id="3e070-108">MAPI appelle votre méthode de fournisseur [IABProvider::Logon](iabprovider-logon.md) au début de chaque session et chaque fois que votre fournisseur est ajouté au profil actif et le client prend en charge la reconfiguration dynamique.</span><span class="sxs-lookup"><span data-stu-id="3e070-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="3e070-109">Lorsque la méthode **IABProvider::Logon** appels MAPI, votre fournisseur de carnet d’adresses commence son processus d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="3e070-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="3e070-110">**Pour mettre en œuvre IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="3e070-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="3e070-111">Initialiser tous les pointeurs de paramètre de sortie passés par MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e070-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="3e070-112">Appeler la méthode **IUnknown::AddRef** de l’objet de la prise en charge pour incrémenter son décompte de références.</span><span class="sxs-lookup"><span data-stu-id="3e070-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="3e070-113">Appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de la prise en charge pour ouvrir la section du profil qui contient les informations de configuration de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3e070-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="3e070-114">Passez la valeur NULL pour le paramètre _lpUID_ et l’indicateur ne si vous souhaitez apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="3e070-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="3e070-115">Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la section profil pour récupérer les propriétés qui ont besoin de votre fournisseur d’ouverture de session, telles que le nom de la table de base de données ou du fichier de données.</span><span class="sxs-lookup"><span data-stu-id="3e070-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="3e070-116">Vérifiez que les propriétés sont tous disponibles et valide.</span><span class="sxs-lookup"><span data-stu-id="3e070-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="3e070-117">Si nécessaire et autorisés, afficher une boîte de dialogue pour inviter l’utilisateur d’effectuer des corrections ou des ajouts aux informations non valides ou absente et appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section profil pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="3e070-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="3e070-118">Les propriétés communes qui doivent être disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e070-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="3e070-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e070-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="3e070-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e070-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="3e070-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e070-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="3e070-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e070-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3e070-123">Ne définissez pas **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e070-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="3e070-124">Au moment de l’ouverture de session, ces propriétés sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e070-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="3e070-125">Si une ou plusieurs propriétés de configuration ne sont pas disponibles, échouer et retourner la valeur MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="3e070-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="3e070-126">Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire un [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="3e070-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="3e070-127">Votre fournisseur peut créer un **MAPIUID** par :</span><span class="sxs-lookup"><span data-stu-id="3e070-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="3e070-128">L’appel de la méthode [IMAPISupport::NewUID](imapisupport-newuid.md) .</span><span class="sxs-lookup"><span data-stu-id="3e070-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="3e070-129">L’appel de la UUIDGEN. Outil EXE pour définir un GUID utilisé par votre fournisseur à inclure dans un des fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3e070-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="3e070-130">Si vous le souhaitez, enregistrer un nouveau **MAPIUID** dans le profil actif en appelant la section profil ** IMAPIProp::SetProps ** méthode.</span><span class="sxs-lookup"><span data-stu-id="3e070-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's ** IMAPIProp::SetProps ** method.</span></span> 
    
9. <span data-ttu-id="3e070-131">Version de la section profil en appelant la méthode **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="3e070-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="3e070-132">Instanciez un nouvel objet d’ouverture de session et définir le contenu du paramètre _lppABLogon_ à l’adresse de ce nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="3e070-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="3e070-133">Puisqu’il est possible de MAPI appeler votre ** ouverture de session ** méthode plusieurs fois au cours d’une session, nous vous conseillons prendre en charge cette possibilité dans votre implémentation lorsqu’ils sont en mesure de créer plusieurs objets d’ouverture de session et garder une trace de chaque objet est créé.</span><span class="sxs-lookup"><span data-stu-id="3e070-133">Because it is possible for MAPI to call your ** Logon ** method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="3e070-134">Prise en charge de plusieurs appels **d’ouverture de session** permet à un utilisateur d’une application cliente, par exemple, pour vous connecter à une session avec différentes identités ou utiliser livraison différentes destinations.</span><span class="sxs-lookup"><span data-stu-id="3e070-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="3e070-135">**L’arrêt** est appelée lorsque la session se termine.</span><span class="sxs-lookup"><span data-stu-id="3e070-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="3e070-136">MAPI appelle votre méthode [IABProvider::Shutdown](iabprovider-shutdown.md) comme une des tâches dernières impliquées dans la fermeture d’une session.</span><span class="sxs-lookup"><span data-stu-id="3e070-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="3e070-137">MAPI a publié tous les objets de connexion de votre fournisseur et, lorsque votre fournisseur reçoit cet appel, il peut supposer qu’il s’agit du dernier appel qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="3e070-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="3e070-138">Dans votre implémentation de **IABProvider::Shutdown**, effectuez un nettoyage final que vous estimez est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3e070-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="3e070-139">Par exemple, votre fournisseur peut appeler **MAPIDeinitIdle** s’il a appelé **MAPIInitIdle** pour utiliser le moteur inactif pendant la session ou de la méthode **IUnknown::Release** de tous les objets qui n’ont pas encore libérée.</span><span class="sxs-lookup"><span data-stu-id="3e070-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="3e070-140">Si votre fournisseur n’a aucun nettoyage final, son implémentation peut être constituée d’une seule ligne de code :</span><span class="sxs-lookup"><span data-stu-id="3e070-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


