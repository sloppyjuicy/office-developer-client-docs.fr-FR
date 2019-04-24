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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348957"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès aux conteneurs du carnet d'adresses. Les applications MAPI et clientes appellent les méthodes de **IABContainer** pour effectuer la résolution de noms et pour créer, copier et supprimer des destinataires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets conteneur du carnet d'adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d'adresses  <br/> |
|Appelé par :  <br/> |Applications MAPI et clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IABContainer  <br/> |
|Type de pointeur:  <br/> |LPABCONT  <br/> |
|Modèle de transaction:  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copie une ou plusieurs entrées, généralement les utilisateurs de messagerie ou les listes de distribution.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Supprime une ou plusieurs entrées, généralement les utilisateurs de messagerie, les listes de distribution ou d'autres conteneurs.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Effectue la résolution de noms pour une ou plusieurs entrées de destinataires.  <br/> |
   
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

L'interface **IABContainer** hérite indirectement de l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) via les interfaces [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) et [IMAPIProp: IUnknown](imapipropiunknown.md) . Les fournisseurs de carnets d'adresses implémentent l'interface **IABContainer** . 
  
Un conteneur de carnet d'adresses peut contenir n'importe quel nombre d'objets utilisateur de messagerie, de listes de distribution et d'autres conteneurs du carnet d'adresses. Comme avec tout conteneur, les clients ou fournisseurs de services peuvent utiliser un conteneur de carnet d'adresses pour ouvrir l'une de ses entrées ou récupérer une table de hiérarchie ou une table de contenu. Les conteneurs du carnet d'adresses fournissent également une résolution de nom et, en fonction du fournisseur, la possibilité d'ajouter, de supprimer ou de modifier des entrées.
  
MAPI définit un conteneur de carnet d'adresses spécial appelé carnet d'adresses personnel (PAB) contenant les entrées copiées à partir d'autres conteneurs. Un PAB est toujours modifiable. Les utilisateurs renseignent généralement leur PAB avec des entrées désignant les destinataires avec lesquels ils communiquent le plus souvent. Un PAB peut également contenir des adresses uniques et des destinataires qui ne font pas encore partie d'un conteneur de carnet d'adresses.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces MAPI](mapi-interfaces.md)

