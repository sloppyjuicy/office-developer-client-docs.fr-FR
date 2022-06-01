---
title: IABContainer IMAPIContainer
description: Cet article décrit IABContainer IMAPIContainer et fournit des méthodes et des propriétés requises.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
ms.openlocfilehash: dea7fb6e57c213d98f78e4eb004d75f23cceabc7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815806"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès aux conteneurs de carnets d’adresses. MapI et les applications clientes appellent les méthodes **d’IABContainer** pour effectuer la résolution de noms et pour créer, copier et supprimer des destinataires. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets conteneur du carnet d’adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |MAPI et applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IABContainer  <br/> |
|Type de pointeur :  <br/> |LPABCONT  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Crée une entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur. |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copie une ou plusieurs entrées, en général des utilisateurs de messagerie ou des listes de distribution. |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Supprime une ou plusieurs entrées, généralement des utilisateurs de messagerie, des listes de distribution ou d’autres conteneurs. |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Effectue la résolution de noms pour une ou plusieurs entrées de destinataire. |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
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

L’interface **IABContainer** hérite indirectement de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) via les interfaces [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) et [IMAPIProp : IUnknown](imapipropiunknown.md) . Les fournisseurs de carnets d’adresses implémentent l’interface **IABContainer** . 
  
Un nombre quelconque d’objets utilisateur de messagerie, de listes de distribution et d’autres conteneurs de carnets d’adresses peuvent exister dans un conteneur de carnet d’adresses. Comme avec n’importe quel conteneur, les clients ou fournisseurs de services peuvent utiliser un conteneur de carnet d’adresses pour ouvrir l’une de ses entrées ou pour récupérer une table de hiérarchie ou une table de contenu. Les conteneurs de carnets d’adresses fournissent également une résolution de noms et, selon le fournisseur, la possibilité d’ajouter, de supprimer ou de modifier des entrées.
  
MAPI définit un conteneur de carnet d’adresses spécial appelé carnet d’adresses personnel (PAB) qui contient les entrées copiées à partir d’autres conteneurs. Un PAB est toujours modifiable. Les utilisateurs remplissent généralement leur PAB avec des entrées désignant les destinataires avec lesquels ils communiquent le plus fréquemment. Un PAB peut également contenir des adresses uniques et les nouveaux destinataires ne font pas encore partie d’un conteneur de carnet d’adresses.
  
## <a name="see-also"></a>Voir aussi

- [Interfaces MAPI](mapi-interfaces.md)

