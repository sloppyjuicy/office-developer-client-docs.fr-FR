---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392185"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne accès aux conteneurs de carnet d’adresses. Applications clientes et MAPI appellent les méthodes **IABContainer** pour effectuer la résolution de noms et pour créer, copier et supprimer des destinataires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets conteneur de carnet d’adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnet d’adresses  <br/> |
|Appelé par :  <br/> |Applications MAPI et client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IABContainer  <br/> |
|Type de pointeur :  <br/> |LPABCONT  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copie une ou plusieurs entrées, les utilisateurs de messagerie en général ou des listes de distribution.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Supprime une ou plusieurs entrées, généralement autres conteneurs, listes de distribution ou les utilisateurs de messagerie.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Effectue la résolution de noms pour une ou plusieurs entrées de destinataire.  <br/> |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
|**Propriétés facultatives**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

L’interface **IABContainer** indirectement hérite de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) par le biais de la [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) et [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces. Fournisseurs de carnet d’adresses implémentent l’interface **IABContainer** . 
  
N’importe quel nombre d’autres conteneurs de carnet d’adresses, des listes de distribution et les objets utilisateur de messagerie peut exister dans un conteneur de carnet d’adresses. Comme avec n’importe quel conteneur, clients ou fournisseurs de services peuvent utiliser un conteneur de carnet d’adresses pour ouvrir une de ses entrées ou récupérer une table de hiérarchie ou une table de contenu. Conteneurs également fournissent la résolution de nom et, selon le fournisseur, la possibilité d’ajouter, supprimer ou modifier des entrées de carnet d’adresses.
  
MAPI définit un conteneur de carnet d’adresses spécial appelé le carnet d’adresses personnel (CAP) qui contient les entrées copiées à partir d’autres conteneurs. Un carnet d’adresses personnel est toujours modifiable. Les utilisateurs remplir généralement leur carnet d’adresses personnel avec des entrées de désigner les destinataires dont ils communiquent plus fréquemment. Un carnet d’adresses personnel peut également contenir des adresses uniques et les nouveaux destinataires n’est pas encore partie de n’importe quel conteneur de carnet d’adresses.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces MAPI](mapi-interfaces.md)

