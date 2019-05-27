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
# <a name="using-multiple-exchange-accounts"></a>Utilisation de plusieurs comptes Exchange

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 et Microsoft Outlook 2013 prennent en charge l’intégration avec plusieurs comptes de messagerie Exchange. Dans Outlook 2010 ou Outlook 2013, un utilisateur peut ajouter deux comptes Exchange au même profil tout en bénéficiant de fonctionnalités Exchange enrichies, telles que la liste d’adresses globale (GAL) publiée, la configuration d’absence du bureau Exchange et le partage de dossiers.
  
Les utilisateurs habitués aux sections de profil MAPI pour Microsoft Office Outlook 2007 et versions antérieures savent que les paramètres Exchange, tels que le nom d’utilisateur et le nom du serveur de messagerie, sont stockés dans la section fixe du profil global Exchange, **pbGlobalProfileSectionGuid**. Dans Outlook 2010 et Outlook 2013, chaque compte Exchange requiert sa propre section de profil pour stocker les paramètres, et dès lors **pbGlobalProfileSectionGuid** est obsolète. 
  
Les paramètres Exchange d’Outlook 2010 et d’Outlook 2013 sont toujours stockés dans le profil, mais un identificateur unique correspondant à la section de profil et contenant ses paramètres est attribué de façon dynamique par profil. Dans le profil, l’emplacement des paramètres Exchange est stocké dans la [propriété canonique PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), qui se trouve dans la section de profil du service de messagerie du compte Exchange. Cette propriété se trouve également dans la section de profil de chaque fournisseur dans ce service de messagerie du compte. L’identificateur unique n’est pas stocké sur le serveur et est différent d’un profil à un autre.
  
Outlook 2010 et Outlook 2013 utilisent **PidTagExchangeProfileSectionId** comme identificateur unique pour spécifier un compte Exchange. Ainsi utilisé, cet identificateur unique est appelé **emsmdbUID**. Pour certaines opérations MAPI et Outlook, une valeur **emsmdbUID** peut être requise afin de spécifier le compte Exchange à utiliser pour l’opération. 
  
Pour prendre en charge plusieurs comptes Exchange, vous devez utiliser certains appels vers de nouvelles fonctions de votre code. Remplacez tous les appels utilisant **entryID** et [IAddrBook:: OpenEntry](iaddrbook-openentry.md) ou [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) sur [IMailUser: IMAPIProp](imailuserimapiprop.md) et [IDistList: IMAPIContainer](idistlistimapicontainer.md) par une des fonctions suivantes. 
  
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
    
## <a name="legacy-support"></a>Prise en charge héritée

Tout client MAPI écrit avant la création de cette nouvelle valeur **emsmdbUID** est encore pris en charge. Ces clients continueront de récupérer la section globale précédente, **pbGlobalProfileSectionGuid**. Les requêtes correspondant à cette section de profil seront redirigées vers un compte Exchange désigné qui gère les requêtes héritées. Le compte qui gère les appels hérités peut être déterminé en examinant la table du service de messagerie et en ajoutant une colonne pour PR_EMSMDB_LEGACY. Seul un service de messagerie présente cette valeur sur true et son **PidTagExchangeProfileSectionId** est appelé valeur **emsmdbUID** héritée.
  
> [!NOTE]
> Les paramètres MAPI configurables, tels que la banque et le compte par défaut, n’ont aucune incidence sur le compte qui gère les appels hérités. Le compte qui gère les appels hérités ne peut pas être configuré. 
  
La valeur **emsmdbUID** du compte hérité est copiée dans la section de profil globale Outlook. Si cette propriété n’existe pas, l’interrogation de la table du service de messagerie détermine le compte correspondant au gestionnaire hérité dans la section de profil global Outlook. 
  
En termes clairs, la section de profil global Outlook diffère de la section de profil global Exchange, et dans Outlook 2010 et Outlook 2013 la section de profil global Exchange n’est plus réellement globale car vous pouvez disposer de plusieurs comptes Exchange. La section de profil global Outlook contient des propriétés sur Outlook, telles que l’état du dossier des éléments utilisés récemment ou l’état de la connexion globale.
  
## <a name="address-book-account-contexts"></a>Contextes de compte de carnet d’adresses

Pour résoudre correctement les adresses avec plusieurs comptes Exchange, utilisez les nouvelles fonctions prenant en compte le contexte de compte de manière à ce que les appels portant sur le carnet d’adresses recherchent le compte Exchange qui convient.
  
Certaines API de carnet d’adresses précédentes ont été déconseillées, car ces API n’étaient pas pleinement compatibles avec Exchange. Ce contexte de compte correspond généralement à une valeur **emsmdbUID**.
  
En plus de la valeur **emsmdbUID**, plusieurs comptes Exchange ont également une valeur **emsabpUID**.
  
1. La valeur **emsmdbUID** identifie le contexte du compte. 
    
2. La valeur **emsabpUID** identifie un fournisseur de carnet d'adresses Exchange. 
    
La valeur **emsabpUID** est généralement utilisée lors de la résolution d’un destinataire. Lors de la résolution d’un destinataire à l’aide de [IAddrBook::ResolveName](iaddrbook-resolvename.md), une ligne de destinataire Exchange contient la propriété **PR_AB_PROVIDERS** (0x3D010102), qui contient la valeur **emsabpUID**. Cette valeur **emsabpUID** identifie le fournisseur de carnet d’adresses Exchange pour le destinataire spécifique. 
  
Si vous souhaitez déterminer la valeur **emsabpUID** d’une valeur **emsmdbUID** spécifique, ouvrez la section de profil correspondant à la valeur **emsmdbUID** et obtenez la propriété **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
Si vous appelez [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), assurez-vous que les destinataires Exchange de la liste que vous transférez contiennent la propriété **PR_AB_PROVIDERS** et que la valeur **emsabpUID** qui correspond au fournisseur de carnet d’adresses auquel appartient le destinataire. Appel [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) sur une ligne que vous avez obtenue de [IAddrBook::ResolveName](iaddrbook-resolvename.md) ne requiert aucune action supplémentaire, mais du code appellera [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) sur les lignes qui contiennent uniquement la propriété **PR_ENTRYID**. Les lignes dans cette situation et autres situations similaires contiennent les propriétés **PR_ENTRYID** et **PR_AB_PROVIDERS** avec la propriété **PR_AB_PROVIDERS** définie sur la valeur **emsabpUID** qui convient.
  
Une description simple du processus de résolution de plusieurs comptes Exchange se présente comme suit :
  
- Compte tenu de l’identificateur unique du service, votre code examine la table de la banque de messages de la propriété **PR_SERVICE_UID** correspondant à celle dont vous disposez. À partir de là, vous pouvez déterminer la propriété **PR_MDB_PROVIDER** qui convient. Cette ligne contient la banque appropriée.
    
- Compte tenu de la valeur **emsmdbUID**, votre code recherche dans la table des services de messages la ligne qui expose la valeur **PidTagExchangeProfileSectionId** correspondant à la valeur **emsmdbUID**.
    
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
  
[PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md)


[Ouverture de la section profil global](https://support.microsoft.com/kb/188482)

