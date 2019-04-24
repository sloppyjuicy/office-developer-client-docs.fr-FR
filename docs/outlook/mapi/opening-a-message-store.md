---
title: Ouverture d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 665c14b285db166e4f2a421d46e57f23e2f7ad52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326221"
---
# <a name="opening-a-message-store"></a>Ouverture d’une banque de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Selon le profil, un client doit ouvrir un ou plusieurs magasins de messages pendant une session standard. L'ouverture d'une banque de messages permet d'accéder à un pointeur vers son implémentation [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) . L'interface **IMsgStore** fournit des méthodes de notification, de création d'affectations de dossiers et d'accès aux dossiers et aux messages. 
  
Les clients ouvrent les banques de messages à l'ouverture de session et lorsqu'un profil est modifié. Si votre client permet aux utilisateurs d'ajouter des banques de messages au profil pendant une session active, vous pouvez les ouvrir immédiatement ou les ignorer jusqu'à la prochaine session. En vous inscrivant aux notifications dans la table de banque de messages, vous serez averti de la disponibilité d'une nouvelle banque de messages.
  
Pour ouvrir une banque de messages, son identificateur d'entrée doit être disponible. La plupart des clients accèdent aux identificateurs d'entrée pour les banques de messages qu'ils souhaitent ouvrir par le biais de la table de banque de messages. Toutefois, certains magasins de messages documentent le format de leurs identificateurs d'entrée, ce qui permet aux clients de contourner la table de banque de messages et de construire l'identificateur d'entrée nécessaire. Ils peuvent transmettre cet identificateur d'entrée directement à [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) et MAPI crée automatiquement une section de profil pour le fournisseur sans l'associer à un service de messagerie. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Récupérer un identificateur d'entrée de la table de banque de messages
  
1. Appelez [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table de banque de messages. 
    
2. Appelez **IMAPITable:: SetColumns** pour limiter le tableau à un petit jeu de colonnes qui inclut les colonnes suivantes: 
    
   - **PR_PROVIDER_DISPLAY** ou **PR_DISPLAY_NAME**
   - Propriétés **PR_ENTRYID** 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Créez une restriction pour filtrer la ligne qui représente la Banque de messages à ouvrir. Pour plus d'informations sur la recherche de la Banque de messages par défaut, consultez [la rubrique ouverture de la Banque de messages par défaut](opening-the-default-message-store.md). Pour rechercher une banque de messages par nom, appliquez l'une des restrictions de propriété suivantes:
    
   - Faire correspondre **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) au nom général de ce type de banque de messages. Par exemple, PR_PROVIDER_DISPLAY peut être défini sur «dossiers personnels».
    
   - Faire correspondre **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) avec le **MAPIUID** spécifique pour ce type de banque de messages. 
    
   - Faire correspondre **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) au nom de cette banque de messages particulière. Par exemple, **PR_DISPLAY_NAME** peut être défini sur «mes messages pour l'année fiscale 2010». 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md) pour extraire la ligne appropriée de la table de banque de messages. L'identificateur d'entrée de la ligne est inclus dans le tableau de valeurs de la propriété pour le membre **aRow** du jeu de lignes pointé par le paramètre _ppRows_ . 
    
5. Appelez [FreeProws](freeprows.md) pour libérer l'ensemble de lignes pointé par _ppRows_.
    
6. Libérez la table de banque de messages en appelant sa méthode **IUnknown:: Release** . 
    
Si vous avez créé un identificateur d'entrée personnalisé pour la Banque de messages à ouvrir, appelez la fonction [WrapStoreEntryID](wrapstoreentryid.md) pour la convertir en identificateur d'entrée standard. 
  
Une fois que vous avez un identificateur d'entrée d'une banque de messages, appelez l'une des méthodes suivantes pour l'ouvrir:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Appelez **OpenMsgStore** si vous devez spécifier une variété d'options spéciales pour la Banque de messages. **OpenMsgStore** vous permet de supprimer l'affichage des boîtes de dialogue, d'identifier la Banque de messages comme étant temporaire ou en tant que magasin de messagerie, de définir les niveaux d'accès et de différer les erreurs. **OpenEntry** vous permet de définir uniquement les niveaux d'accès et les erreurs de report. 
  
La définition de l'indicateur MDB_NO_MAIL indique à MAPI que la Banque de messages ne sera pas utilisée pour l'envoi ou la réception de messages. MAPI n'informe pas le spouleur MAPI de l'existence de cette banque de messages. L'indicateur MDB_TEMPORARY désigne une banque de messages comme étant temporaire, ce qui signifie qu'elle ne peut pas être utilisée pour stocker des informations permanentes. Les banques de messages temporaires n'apparaissent pas dans la table de banque de messages. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

