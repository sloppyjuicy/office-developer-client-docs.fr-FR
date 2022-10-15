---
title: Utilisation de plusieurs comptes Exchange
description: Décrit comment utiliser plusieurs comptes Exchange dans Outlook 2013 et Outlook 2016, avec des liens vers des documents de référence.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
ms.openlocfilehash: 7011622301462fd9e5434e3392d1d638001f63b5
ms.sourcegitcommit: b6d8fc4db483ecd1a3247a6cb3377f5b52c44cfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2022
ms.locfileid: "68574321"
---
# <a name="using-multiple-exchange-accounts"></a>Utilisation de plusieurs comptes Exchange

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 et Microsoft Outlook 2013 prennent en charge l’intégration à plusieurs comptes de messagerie Exchange. Dans Outlook 2010 ou Outlook�2013, un utilisateur peut ajouter deux comptes exchange sur le m�me profil et quand m�me profiter de riches fonctionnalit�s Exchange telles que la liste d'adresses globale publi� (LAG), la configuration de Exchange d'absence et le partage des dossiers.
  
Ceux qui connaissent les sections de profil MAPI pour Microsoft Office Outlook 2007 et les versions antérieures savent que les paramètres Exchange, tels que le nom d’utilisateur et le nom du serveur d’e-mail, sont stockés dans la section profil global Exchange fixe, **pbGlobalProfileSectionGuid**. Dans Outlook 2010 et Outlook�2013, chaque compte Exchange a besoin de sa propre section de profil pour stocker les param�tres, rendant l' **pbGlobalProfileSectionGuid** obsol�te. 
  
Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.
  
Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation. 
  
In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>Prise en charge h�rit�e

Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.
  
> [!NOTE]
> Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured. 
  
The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section. 
  
To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.
  
## <a name="address-book-account-contexts"></a>Contextes de compte de carnet d'adresses

R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�.
  
Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.
  
En plus de la **emsmdbUID**, plusieurs comptes Exchange ont �galement un **emsabpUID**.
  
1. La valeur **emsmdbUID** identifie le contexte du compte. 
    
2. La valeur **emsabpUID** identifie un fournisseur de carnet d'adresses Exchange. 
    
The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient. 
  
Si vous souhaitez d�terminer la valeur de **emsabpUID** pour un particulier **emsmdbUID**, ouvrez la section de profil pour la **emsmdbUID** et obtenir la propri�t� **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.
  
Description de la proc�dure de r�solution de plusieurs comptes Exchange simple est comme suit :
  
- Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.
    
- �tant donn� un **emsmdbUID**, votre code se pr�sente dans le tableau de services de message pour la ligne qui expose les **PidTagExchangeProfileSectionId** qui correspond � la **emsmdbUID**.
    
## <a name="see-also"></a>Voir aussi



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[Propri�t� canonique PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md)


[How To Open the Global Profile Section](/training/paths/configure-user-device-profiles/)
