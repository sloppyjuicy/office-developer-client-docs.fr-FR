---
title: Utilisation de plusieurs comptes Exchange
description: Décrit comment utiliser plusieurs comptes Exchange dans Outlook 2013 et Outlook 2016, avec des liens vers des documents de référence.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
ms.openlocfilehash: c1d699ffb842d4139d297fa3f8c3046a5fd9d19f
ms.sourcegitcommit: 600f0dc552b725f98f3354d42feefc39be9c354c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2022
ms.locfileid: "66577315"
---
# <a name="using-multiple-exchange-accounts"></a>Utilisation de plusieurs comptes Exchange

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 et Microsoft Outlook 2013 prennent en charge l’intégration à plusieurs comptes de messagerie Exchange. Dans Outlook 2010 ou Outlook�2013, un utilisateur peut ajouter deux comptes exchange sur le m�me profil et quand m�me profiter de riches fonctionnalit�s Exchange telles que la liste d'adresses globale publi� (LAG), la configuration de Exchange d'absence et le partage des dossiers.
  
Ceux qui connaissent les sections de profil MAPI pour Microsoft Office Outlook 2007 et les versions antérieures savent que les paramètres Exchange, tels que le nom d’utilisateur et le nom du serveur d’e-mail, sont stockés dans la section profil global Exchange fixe, **pbGlobalProfileSectionGuid**. Dans Outlook 2010 et Outlook�2013, chaque compte Exchange a besoin de sa propre section de profil pour stocker les param�tres, rendant l' **pbGlobalProfileSectionGuid** obsol�te. 
  
Outlook 2010 and Outlook�2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [Propri�t� canonique PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.
  
Outlook 2010 et Outlook�2013 utilisent le **PidTagExchangeProfileSectionId** comme un identificateur unique pour sp�cifier un compte Exchange. Lorsqu'il est utilis� de cette mani�re, cet identificateur unique est appel� le **emsmdbUID**. Pour certaines op�rations MAPI et Outlook, un **emsmdbUID** peut �tre requis pour sp�cifier quel compte Exchange doit �tre utilis� pour l'op�ration. 
  
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

Les clients MAPI d'�criture avant la cr�ation de cette nouvelle section **emsmdbUID** sont toujours pris en charge. Ces clients continuera � r�cup�rer la pr�c�dente section globale, **pbGlobalProfileSectionGuid**. Requ�tes de cette section de profil seront redirig�s vers un seul compte Exchange d�sign� qui g�re les recherches h�rit�s. Le compte qui g�re les appels h�rit�s peut �tre d�termin� en examinant le tableau de service de message et en ajoutant une colonne pour PR_EMSMDB_LEGACY. Seulement un service de message sont d�finis sur true et ses **PidTagExchangeProfileSectionId** est appel� le h�rit� **emsmdbUID**.
  
> [!NOTE]
> [!REMARQUE] Param�tres MAPI configurables tels que la banque par d�faut et le compte par d�faut ont aucun effet sur lequel compte g�re les appels h�rit�s. Le compte qui g�re les appels h�rit�s ne peut pas �tre configur�. 
  
La **emsmdbUID** du compte h�rit� est copi� dans la Section profil globale Outlook. Si cette propri�t� n'existe pas, interrogation de la table de services de message sont alors d�terminer quel compte est le gestionnaire h�rit� et d�finir la valeur dans la Section profil globale Outlook. 
  
Pour �tre d�sactivez, l' Outlook que Global Section profil diff�re de la Section de profil Global Exchange, et dans Outlook 2010 et Outlook�2013 la Section globale Exchange n'est plus vraiment globale, car vous pouvez avoir plusieurs comptes Exchange. La section profil Global Outlook contient les propri�t�s sur Outlook, telles que l'�tat du dossier R�cemment ou l'�tat de la connexion globale.
  
## <a name="address-book-account-contexts"></a>Contextes de compte de carnet d'adresses

R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�.
  
Certaines pr�c�dentes du carnet d'adresses Qu'api ont �t� d�conseill�es, car les API n'ont pas �taient enti�rement plusieurs Exchange capable. Le contexte de ce compte est g�n�ralement un **emsmdbUID**.
  
En plus de la **emsmdbUID**, plusieurs comptes Exchange ont �galement un **emsabpUID**.
  
1. La valeur **emsmdbUID** identifie le contexte du compte. 
    
2. La valeur **emsabpUID** identifie un fournisseur de carnet d'adresses Exchange. 
    
The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient. 
  
Si vous souhaitez d�terminer la valeur de **emsabpUID** pour un particulier **emsmdbUID**, ouvrez la section de profil pour la **emsmdbUID** et obtenir la propri�t� **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.
  
Description de la proc�dure de r�solution de plusieurs comptes Exchange simple est comme suit :
  
- �tant donn� l'identificateur unique du service, votre code se pr�sente dans la table de la banque de messages de la propri�t� **PR_SERVICE_UID** qui correspond � celui dont vous disposez. � partir de l�, vous pouvez d�terminer la correcte **PR_MDB_PROVIDER**. Cette ligne contient la banque appropri�e.
    
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


[How To Open the Global Profile Section](/learn/paths/configure-user-device-profiles/)

