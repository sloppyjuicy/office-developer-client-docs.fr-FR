---
title: Utilisation de plusieurs comptes Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 3c0392cd6a885900c1a305cd1cd816a5925745a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398590"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="08205-103">Utilisation de plusieurs comptes Exchange</span><span class="sxs-lookup"><span data-stu-id="08205-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="08205-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08205-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08205-105">Microsoft Outlook 2010 et Microsoft Outlook 2013 prend en charge l’intégration avec plusieurs comptes de messagerie exchange.</span><span class="sxs-lookup"><span data-stu-id="08205-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="08205-106">Dans Outlook 2010 ou Outlook�2013, un utilisateur peut ajouter deux comptes exchange sur le m�me profil et quand m�me profiter de riches fonctionnalit�s Exchange telles que la liste d'adresses globale publi� (LAG), la configuration de Exchange d'absence et le partage des dossiers.</span><span class="sxs-lookup"><span data-stu-id="08205-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="08205-107">Ces familiarisé avec les sections de profil MAPI pour Microsoft Office Outlook 2007 et versions antérieures savoir que les paramètres Exchange, telles que le nom d’utilisateur de messagerie et le nom du serveur, sont stockés dans la section profil Global Exchange fixe, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="08205-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the email user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="08205-108">Pour plus d'informations sur le profil Global Exchange, voir [comment ouvrir la Section profil Global](https://support.microsoft.com/kb/188482).</span><span class="sxs-lookup"><span data-stu-id="08205-108">For more information about the Exchange Global Profile, see [How To Open the Global Profile Section](https://support.microsoft.com/kb/188482).</span></span> <span data-ttu-id="08205-109">Dans Outlook 2010 et Outlook�2013, chaque compte Exchange a besoin de sa propre section de profil pour stocker les param�tres, rendant l' **pbGlobalProfileSectionGuid** obsol�te.</span><span class="sxs-lookup"><span data-stu-id="08205-109">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="08205-p103">Outlook 2010 and Outlook�2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [Propri�t� canonique PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span><span class="sxs-lookup"><span data-stu-id="08205-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="08205-p104">Outlook 2010 et Outlook�2013 utilisent le **PidTagExchangeProfileSectionId** comme un identificateur unique pour sp�cifier un compte Exchange. Lorsqu'il est utilis� de cette mani�re, cet identificateur unique est appel� le **emsmdbUID**. Pour certaines op�rations MAPI et Outlook, un **emsmdbUID** peut �tre requis pour sp�cifier quel compte Exchange doit �tre utilis� pour l'op�ration.</span><span class="sxs-lookup"><span data-stu-id="08205-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="08205-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span><span class="sxs-lookup"><span data-stu-id="08205-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="08205-119">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="08205-119">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="08205-120">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="08205-120">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="08205-121">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="08205-121">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="08205-122">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="08205-122">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="08205-123">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="08205-123">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="08205-124">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="08205-124">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="08205-125">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="08205-125">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="08205-126">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="08205-126">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="08205-127">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="08205-127">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="08205-128">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="08205-128">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="08205-129">Prise en charge h�rit�e</span><span class="sxs-lookup"><span data-stu-id="08205-129">Legacy support</span></span>

<span data-ttu-id="08205-p106">Les clients MAPI d'�criture avant la cr�ation de cette nouvelle section **emsmdbUID** sont toujours pris en charge. Ces clients continuera � r�cup�rer la pr�c�dente section globale, **pbGlobalProfileSectionGuid**. Requ�tes de cette section de profil seront redirig�s vers un seul compte Exchange d�sign� qui g�re les recherches h�rit�s. Le compte qui g�re les appels h�rit�s peut �tre d�termin� en examinant le tableau de service de message et en ajoutant une colonne pour PR_EMSMDB_LEGACY. Seulement un service de message sont d�finis sur true et ses **PidTagExchangeProfileSectionId** est appel� le h�rit� **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="08205-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="08205-p107">[!REMARQUE] Param�tres MAPI configurables tels que la banque par d�faut et le compte par d�faut ont aucun effet sur lequel compte g�re les appels h�rit�s. Le compte qui g�re les appels h�rit�s ne peut pas �tre configur�.</span><span class="sxs-lookup"><span data-stu-id="08205-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="08205-p108">La **emsmdbUID** du compte h�rit� est copi� dans la Section profil globale Outlook. Si cette propri�t� n'existe pas, interrogation de la table de services de message sont alors d�terminer quel compte est le gestionnaire h�rit� et d�finir la valeur dans la Section profil globale Outlook.</span><span class="sxs-lookup"><span data-stu-id="08205-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="08205-p109">Pour �tre d�sactivez, l' Outlook que Global Section profil diff�re de la Section de profil Global Exchange, et dans Outlook 2010 et Outlook�2013 la Section globale Exchange n'est plus vraiment globale, car vous pouvez avoir plusieurs comptes Exchange. La section profil Global Outlook contient les propri�t�s sur Outlook, telles que l'�tat du dossier R�cemment ou l'�tat de la connexion globale.</span><span class="sxs-lookup"><span data-stu-id="08205-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="08205-141">Contextes de compte de carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="08205-141">Address Book Account Contexts</span></span>

<span data-ttu-id="08205-142">R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�.</span><span class="sxs-lookup"><span data-stu-id="08205-142">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="08205-p110">Certaines pr�c�dentes du carnet d'adresses Qu'api ont �t� d�conseill�es, car les API n'ont pas �taient enti�rement plusieurs Exchange capable. Le contexte de ce compte est g�n�ralement un **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="08205-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="08205-145">En plus de la **emsmdbUID**, plusieurs comptes Exchange ont �galement un **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="08205-145">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="08205-146">La valeur **emsmdbUID** identifie le contexte du compte.</span><span class="sxs-lookup"><span data-stu-id="08205-146">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="08205-147">La valeur **emsabpUID** identifie un fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="08205-147">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="08205-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span><span class="sxs-lookup"><span data-stu-id="08205-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="08205-151">Si vous souhaitez d�terminer la valeur de **emsabpUID** pour un particulier **emsmdbUID**, ouvrez la section de profil pour la **emsmdbUID** et obtenir la propri�t� **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="08205-151">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="08205-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="08205-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="08205-155">Description de la proc�dure de r�solution de plusieurs comptes Exchange simple est comme suit :</span><span class="sxs-lookup"><span data-stu-id="08205-155">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="08205-p113">�tant donn� l'identificateur unique du service, votre code se pr�sente dans la table de la banque de messages de la propri�t� **PR_SERVICE_UID** qui correspond � celui dont vous disposez. � partir de l�, vous pouvez d�terminer la correcte **PR_MDB_PROVIDER**. Cette ligne contient la banque appropri�e.</span><span class="sxs-lookup"><span data-stu-id="08205-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="08205-159">�tant donn� un **emsmdbUID**, votre code se pr�sente dans le tableau de services de message pour la ligne qui expose les **PidTagExchangeProfileSectionId** qui correspond � la **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="08205-159">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08205-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08205-160">See also</span></span>



[<span data-ttu-id="08205-161">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="08205-161">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="08205-162">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="08205-162">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="08205-163">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="08205-163">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="08205-164">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="08205-164">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="08205-165">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="08205-165">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="08205-166">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="08205-166">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="08205-167">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="08205-167">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="08205-168">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="08205-168">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="08205-169">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="08205-169">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="08205-170">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="08205-170">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="08205-171">Propri�t� canonique PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="08205-171">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="08205-172">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="08205-172">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

