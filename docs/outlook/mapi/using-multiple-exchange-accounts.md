---
title: Utilisation de plusieurs comptes Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329651"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="8bf38-103">Utilisation de plusieurs comptes Exchange</span><span class="sxs-lookup"><span data-stu-id="8bf38-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="8bf38-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bf38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bf38-105">Microsoft Outlook 2010 et Microsoft Outlook 2013 prennent en charge l’intégration avec plusieurs comptes de messagerie Exchange.</span><span class="sxs-lookup"><span data-stu-id="8bf38-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange e-mail accounts.</span></span> <span data-ttu-id="8bf38-106">Dans Outlook 2010 ou Outlook 2013, un utilisateur peut ajouter deux comptes Exchange au même profil tout en bénéficiant de fonctionnalités Exchange enrichies, telles que la liste d’adresses globale (GAL) publiée, la configuration d’absence du bureau Exchange et le partage de dossiers.</span><span class="sxs-lookup"><span data-stu-id="8bf38-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="8bf38-107">Les utilisateurs habitués aux sections de profil MAPI pour Microsoft Office Outlook 2007 et versions antérieures savent que les paramètres Exchange, tels que le nom d’utilisateur et le nom du serveur de messagerie, sont stockés dans la section fixe du profil global Exchange, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="8bf38-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the e-mail user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="8bf38-108">Dans Outlook 2010 et Outlook 2013, chaque compte Exchange requiert sa propre section de profil pour stocker les paramètres, et dès lors **pbGlobalProfileSectionGuid** est obsolète.</span><span class="sxs-lookup"><span data-stu-id="8bf38-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="8bf38-p103">Les paramètres Exchange d’Outlook 2010 et d’Outlook 2013 sont toujours stockés dans le profil, mais un identificateur unique correspondant à la section de profil et contenant ses paramètres est attribué de façon dynamique par profil. Dans le profil, l’emplacement des paramètres Exchange est stocké dans la [propriété canonique PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), qui se trouve dans la section de profil du service de messagerie du compte Exchange. Cette propriété se trouve également dans la section de profil de chaque fournisseur dans ce service de messagerie du compte. L’identificateur unique n’est pas stocké sur le serveur et est différent d’un profil à un autre.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="8bf38-p104">Outlook 2010 et Outlook 2013 utilisent **PidTagExchangeProfileSectionId** comme identificateur unique pour spécifier un compte Exchange. Ainsi utilisé, cet identificateur unique est appelé **emsmdbUID**. Pour certaines opérations MAPI et Outlook, une valeur **emsmdbUID** peut être requise afin de spécifier le compte Exchange à utiliser pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="8bf38-p105">Pour prendre en charge plusieurs comptes Exchange, vous devez utiliser certains appels vers de nouvelles fonctions de votre code. Remplacez tous les appels utilisant **entryID** et [IAddrBook:: OpenEntry](iaddrbook-openentry.md) ou [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) sur [IMailUser: IMAPIProp](imailuserimapiprop.md) et [IDistList: IMAPIContainer](idistlistimapicontainer.md) par une des fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="8bf38-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="8bf38-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="8bf38-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="8bf38-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="8bf38-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="8bf38-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="8bf38-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="8bf38-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="8bf38-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="8bf38-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="8bf38-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="8bf38-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="8bf38-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="8bf38-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="8bf38-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="8bf38-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="8bf38-128">Prise en charge héritée</span><span class="sxs-lookup"><span data-stu-id="8bf38-128">Legacy support</span></span>

<span data-ttu-id="8bf38-p106">Tout client MAPI écrit avant la création de cette nouvelle valeur **emsmdbUID** est encore pris en charge. Ces clients continueront de récupérer la section globale précédente, **pbGlobalProfileSectionGuid**. Les requêtes correspondant à cette section de profil seront redirigées vers un compte Exchange désigné qui gère les requêtes héritées. Le compte qui gère les appels hérités peut être déterminé en examinant la table du service de messagerie et en ajoutant une colonne pour PR_EMSMDB_LEGACY. Seul un service de messagerie présente cette valeur sur true et son **PidTagExchangeProfileSectionId** est appelé valeur **emsmdbUID** héritée.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8bf38-p107">Les paramètres MAPI configurables, tels que la banque et le compte par défaut, n’ont aucune incidence sur le compte qui gère les appels hérités. Le compte qui gère les appels hérités ne peut pas être configuré.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="8bf38-p108">La valeur **emsmdbUID** du compte hérité est copiée dans la section de profil globale Outlook. Si cette propriété n’existe pas, l’interrogation de la table du service de messagerie détermine le compte correspondant au gestionnaire hérité dans la section de profil global Outlook.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="8bf38-p109">En termes clairs, la section de profil global Outlook diffère de la section de profil global Exchange, et dans Outlook 2010 et Outlook 2013 la section de profil global Exchange n’est plus réellement globale car vous pouvez disposer de plusieurs comptes Exchange. La section de profil global Outlook contient des propriétés sur Outlook, telles que l’état du dossier des éléments utilisés récemment ou l’état de la connexion globale.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="8bf38-140">Contextes de compte de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="8bf38-140">Address Book Account Contexts</span></span>

<span data-ttu-id="8bf38-141">Pour résoudre correctement les adresses avec plusieurs comptes Exchange, utilisez les nouvelles fonctions prenant en compte le contexte de compte de manière à ce que les appels portant sur le carnet d’adresses recherchent le compte Exchange qui convient.</span><span class="sxs-lookup"><span data-stu-id="8bf38-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="8bf38-p110">Certaines API de carnet d’adresses précédentes ont été déconseillées, car ces API n’étaient pas pleinement compatibles avec Exchange. Ce contexte de compte correspond généralement à une valeur **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="8bf38-144">En plus de la valeur **emsmdbUID**, plusieurs comptes Exchange ont également une valeur **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="8bf38-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="8bf38-145">La valeur **emsmdbUID** identifie le contexte du compte.</span><span class="sxs-lookup"><span data-stu-id="8bf38-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="8bf38-146">La valeur **emsabpUID** identifie un fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="8bf38-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="8bf38-p111">La valeur **emsabpUID** est généralement utilisée lors de la résolution d’un destinataire. Lors de la résolution d’un destinataire à l’aide de [IAddrBook::ResolveName](iaddrbook-resolvename.md), une ligne de destinataire Exchange contient la propriété **PR_AB_PROVIDERS** (0x3D010102), qui contient la valeur **emsabpUID**. Cette valeur **emsabpUID** identifie le fournisseur de carnet d’adresses Exchange pour le destinataire spécifique.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="8bf38-150">Si vous souhaitez déterminer la valeur **emsabpUID** d’une valeur **emsmdbUID** spécifique, ouvrez la section de profil correspondant à la valeur **emsmdbUID** et obtenez la propriété **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="8bf38-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="8bf38-p112">Si vous appelez [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), assurez-vous que les destinataires Exchange de la liste que vous transférez contiennent la propriété **PR_AB_PROVIDERS** et que la valeur **emsabpUID** qui correspond au fournisseur de carnet d’adresses auquel appartient le destinataire. Appel [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) sur une ligne que vous avez obtenue de [IAddrBook::ResolveName](iaddrbook-resolvename.md) ne requiert aucune action supplémentaire, mais du code appellera [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) sur les lignes qui contiennent uniquement la propriété **PR_ENTRYID**. Les lignes dans cette situation et autres situations similaires contiennent les propriétés **PR_ENTRYID** et **PR_AB_PROVIDERS** avec la propriété **PR_AB_PROVIDERS** définie sur la valeur **emsabpUID** qui convient.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="8bf38-154">Une description simple du processus de résolution de plusieurs comptes Exchange se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="8bf38-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="8bf38-p113">Compte tenu de l’identificateur unique du service, votre code examine la table de la banque de messages de la propriété **PR_SERVICE_UID** correspondant à celle dont vous disposez. À partir de là, vous pouvez déterminer la propriété **PR_MDB_PROVIDER** qui convient. Cette ligne contient la banque appropriée.</span><span class="sxs-lookup"><span data-stu-id="8bf38-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="8bf38-158">Compte tenu de la valeur **emsmdbUID**, votre code recherche dans la table des services de messages la ligne qui expose la valeur **PidTagExchangeProfileSectionId** correspondant à la valeur **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="8bf38-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bf38-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bf38-159">See also</span></span>



[<span data-ttu-id="8bf38-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="8bf38-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="8bf38-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="8bf38-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="8bf38-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="8bf38-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="8bf38-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="8bf38-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="8bf38-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="8bf38-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="8bf38-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="8bf38-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="8bf38-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="8bf38-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="8bf38-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="8bf38-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="8bf38-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="8bf38-170">PidTagExchangeProfileSectionId Canonical Property</span><span class="sxs-lookup"><span data-stu-id="8bf38-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="8bf38-171">Ouverture de la section profil global</span><span class="sxs-lookup"><span data-stu-id="8bf38-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

