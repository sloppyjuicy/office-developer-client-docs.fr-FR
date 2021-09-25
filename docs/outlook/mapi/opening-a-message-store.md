---
title: Ouverture d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 428b5b59a5f1a73ae440e4406a5a2971fed26b39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610096"
---
# <a name="opening-a-message-store"></a>Ouverture d’une banque de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Selon le profil, un client doit ouvrir une ou plusieurs magasins de messages au cours d’une session classique. L’ouverture d’une magasin de messages signifie accéder à un pointeur vers son [implémentation IMsgStore : IMAPIProp.](imsgstoreimapiprop.md) **L’interface IMsgStore** fournit des méthodes de notification, d’affectation de dossiers et d’accès aux dossiers et aux messages. 
  
Clients open message stores at logon and when a profile is being modified. Si votre client permet aux utilisateurs d’ajouter des magasins de messages au profil pendant une session active, vous pouvez les ouvrir immédiatement ou les ignorer jusqu’à la prochaine session. En vous enregistrant pour les notifications sur la table de la boutique de messages, vous serez averti de la disponibilité d’une nouvelle magasin de messages.
  
Pour ouvrir une magasin de messages, son identificateur d’entrée doit être disponible. La plupart des clients accèdent aux identificateurs d’entrée pour les magasins de messages qu’ils souhaitent ouvrir via la table de la boutique de messages. Toutefois, certains messages stockent le format de leurs identificateurs d’entrée, ce qui permet aux clients de contourner la table de la boutique de messages et de construire l’identificateur d’entrée nécessaire. Ils peuvent transmettre cet identificateur d’entrée directement à [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) et MAPI crée automatiquement une section de profil pour le fournisseur sans l’associer à un service de message. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Récupérer un identificateur d’entrée à partir de la table de la boutique de messages
  
1. Appelez [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table de la boutique de messages. 
    
2. Appelez **IMAPITable::SetColumns** pour limiter le tableau à un petit jeu de colonnes qui inclut les colonnes suivantes : 
    
   - **PR_PROVIDER_DISPLAY** ou **PR_DISPLAY_NAME**
   - **PR_ENTRYID** propriétés 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Créez une restriction pour filtrer la ligne qui représente la magasin de messages à ouvrir. Pour plus d’informations sur la recherche de la magasin de messages par défaut, voir [Ouverture de la boutique de messages par défaut.](opening-the-default-message-store.md) Pour rechercher un magasin de messages par nom, appliquez l’une des restrictions de propriété suivantes :
    
   - Correspondez **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) avec le nom général de ce type de magasin de messages. Par exemple, PR_PROVIDER_DISPLAY peut être définie sur « Dossiers personnels ».
    
   - Faire **correspondre PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) avec le **MAPIUID** spécifique pour ce type de magasin de messages. 
    
   - Faire **correspondre PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom de cette boutique de messages particulière. Par exemple, **PR_DISPLAY_NAME** peut être définie sur « Mes messages pour l’année fiscale 2010 ». 
    
4. Appelez [HrQueryAllRows pour](hrqueryallrows.md) récupérer la ligne appropriée à partir de la table de la boutique de messages. L’identificateur d’entrée de la ligne sera inclus dans le tableau des valeurs de propriété pour le membre **aRow** du jeu de lignes pointé par le _paramètre pprows._ 
    
5. Appelez [FreeProws pour](freeprows.md) libérer le jeu de lignes pointé par  _pprows_.
    
6. Release the message store table by calling its **IUnknown::Release** method. 
    
Si vous avez créé un identificateur d’entrée personnalisé pour l’ouverture de la boutique de messages, appelez la fonction [WrapStoreEntryID](wrapstoreentryid.md) pour la convertir en identificateur d’entrée standard. 
  
Une fois que vous avez l’identificateur d’entrée d’une boutique de messages, appelez l’une des méthodes suivantes pour l’ouvrir :
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Appelez **OpenMsgStore** si vous devez spécifier plusieurs options spéciales pour la boutique de messages. **OpenMsgStore** vous permet de supprimer l’affichage des boîtes de dialogue, d’identifier la magasin de messages comme temporaire ou comme magasin de non-hébergement, de définir des niveaux d’accès et de différer les erreurs. **OpenEntry vous permet** uniquement de définir des niveaux d’accès et de différer les erreurs. 
  
La définition MDB_NO_MAIL’indicateur de message indique à MAPI que la boutique de messages ne sera pas utilisée pour l’envoi ou la réception de messages. MAPI n’informe pas lepooler MAPI de l’existence de ce magasin de messages. L MDB_TEMPORARY désigne une collection de messages comme temporaire, ce qui signifie qu’elle ne peut pas être utilisée pour stocker des informations permanentes. Les magasins de messages temporaires n’apparaissent pas dans la table de la boutique de messages. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

