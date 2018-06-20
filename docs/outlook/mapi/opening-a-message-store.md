---
title: L’ouverture d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 39d6df6db329abf7509f816165341ea0eda8331b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784918"
---
# <a name="opening-a-message-store"></a>L’ouverture d’une banque de messages

**S’applique à**: Outlook 
  
En fonction du profil, un client vous devrez ouvrir une ou plusieurs bases de messages pendant une session typique. L’ouverture d’une banque de messages signifie que l’accès à un pointeur vers son [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implémentation. L’interface **IMsgStore** fournit des méthodes de notification, rendant les affectations de dossiers et l’accès aux dossiers et messages. 
  
Les clients ouvrent des banques de messages à l’ouverture de session et lors d’un profil est en cours de modification. Si votre client permet aux utilisateurs d’ajouter des banques de messages au profil pendant une session active, vous pouvez les ouvrir immédiatement ou les ignorer jusqu'à la prochaine session. En enregistrant des notifications sur la table, un message vous avertit de la disponibilité d’une nouvelle banque de messages.
  
Pour ouvrir une banque de messages, vous devez disposer de son identificateur d’entrée disponible. Accéder à la plupart des clients les identificateurs d’entrée pour les banques de messages qu’ils souhaitent ouvrir par le biais de la table. Toutefois, certains messages stocke le format de leurs identificateurs d’entrée, ce qui permet aux clients de contournement de la table et construire l’identificateur d’entrée nécessaire de document. Ils peuvent passer cet identificateur d’entrée directement au [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) et MAPI crée automatiquement une section de profil pour le fournisseur sans l’associer à n’importe quel service de message. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Récupérer un identificateur d’entrée de la table de la banque de message
  
1. Appelez [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table. 
    
2. Appelez **IMAPITable::SetColumns** pour limiter la table à un ensemble de colonne de petite taille qui inclut les colonnes suivantes : 
    
   - **PR_PROVIDER_DISPLAY** ou **PR_DISPLAY_NAME**
   - Propriétés **PR_ENTRYID** 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Créer une restriction pour filtrer la ligne qui représente la banque de messages à ouvrir. Pour plus d’informations sur la recherche de la banque de messages par défaut, voir [l’ouverture de la banque de messages par défaut](opening-the-default-message-store.md). Pour rechercher une banque de messages par un nom, appliquez une des restrictions de propriété suivantes :
    
   - Correspondance **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) avec le nom général pour ce type de banque de messages. Par exemple, PR_PROVIDER_DISPLAY peut être définie sur « Dossiers personnels ».
    
   - Correspondance **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) avec l' spécifique **MAPIUID** pour ce type de banque de messages. 
    
   - Correspondance **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom de cette banque de messages donnée. Par exemple, **PR_DISPLAY_NAME** peut être définie à « Mes Messages pour l’année fiscale 2010 ». 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer la ligne appropriée à partir de la table. L’identificateur d’entrée de la ligne sera être inclus dans le tableau de valeurs de propriété de membre de l’ensemble de lignes indiqué par le paramètre _pprows_ **: UGAL** . 
    
5. Appelez [FreeProws](freeprows.md) pour libérer le jeu de lignes indiqué par _pprows_.
    
6. Version de la table de banque de messages en appelant la méthode **IUnknown::Release** . 
    
Si vous avez créé un identificateur d’entrée personnalisée pour la banque de messages à ouvrir, appelez la fonction [WrapStoreEntryID](wrapstoreentryid.md) pour convertir en un identificateur d’entrée standard. 
  
Une fois que vous avez identificateur d’entrée d’une banque de messages, appelez l’une des méthodes suivantes pour l’ouvrir :
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Appelez **OpenMsgStore** si vous devez spécifier une série d’options spéciales pour la banque de messages. **OpenMsgStore** vous permet de supprimer l’affichage des boîtes de dialogue, identifier la banque de messages en tant que fichier temporaire ou un magasin non-messagerie, définir des niveaux d’accès et de différer des erreurs. **OpenEntry** vous permet uniquement aux niveaux d’accès définis et différer des erreurs. 
  
Définition de la MDB_NO_MAIL indicateur indique à MAPI que la banque de messages ne sera pas être utilisée pour envoyer ou recevoir de messages. MAPI n’informe pas le spouleur MAPI sur l’existence de cette banque de messages. L’indicateur MDB_TEMPORARY désigne une banque de messages comme temporaire, ce qui implique qu’il ne peut être utilisé pour stocker les informations permanentes. Banques de messages temporaire n’apparaissent pas dans la table. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

