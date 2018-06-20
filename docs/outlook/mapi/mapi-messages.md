---
title: Messages MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1146fa0441d0b55a7610368324489bd3a6bb24e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784646"
---
# <a name="mapi-messages"></a>Messages MAPI

  
  
**S’applique à**: Outlook 
  
Les messages sont transmis à partir de l’application d’un client vers une autre via le spouleur MAPI et les fournisseurs de services par un système de messagerie MAPI d’objets. Presque chaque composant MAPI fonctionne avec des messages. Clients permettent aux utilisateurs de créer, enregistrer, envoyer et supprimer des messages de plus de copier et des faire passer d’un dossier à un autre. Fournisseurs de banque de messages sont responsables de la gestion des messages et de remise des messages pour le spouleur MAPI ou un fournisseur de transport. Le spouleur MAPI déplace les messages vers un fournisseur de transport approprié, tandis que les fournisseurs de transport gérer la remise et la réception de messages vers et depuis un système de messagerie et définir des propriétés de l’option destinataire et le message. Fournisseurs de carnet d’adresses manipuler indirectement messages, prise en charge des propriétés qui décrivent les destinataires du message.
  
Les messages sont stockés dans des dossiers dans une banque de messages, généralement les dossiers créés dans le dossier racine de message interpersonnel (IPM). Les messages sont généralement stockées au même niveau que la boîte de réception IPM standard, éléments envoyés, éléments supprimés et les dossiers boîte d’envoi, ou à des niveaux inférieurs dans la hiérarchie. Toutefois, les messages peuvent également être stockés en dehors de la sous-arborescence IPM.
  
Les messages créés dans la sous-arborescence IPM standard ont un contenu standard (autrement dit, contenu qui est visibles par l’utilisateur d’une application cliente). Les rapports et les notes sont des exemples de messages qui ont un contenu standard. Les messages peuvent également être créées avec le contenu associé ou le contenu qui n’est pas visibles dans le client par défaut. Dossiers prennent en charge deux tables d’un contenu différent pour contenir les différents types de messages : une norme de contenu de table pour les messages standards et un contenu associé pour les messages associés. Car MAPI ne définit pas les normes pour le contenu des messages associés, ils peuvent contenir des informations arbitraires. 
  
Un message peut contenir des données supplémentaires, sous la forme d’un fichier, un autre message ou un objet OLE, lui est associé. Ces données supplémentaires, qui sont appelées une pièce jointe, s’affiche sous forme d’icône ou, pour un message au format RTF, en tant que métafichier dans le texte du message. Un message peut contenir zéro, une ou plusieurs pièces jointes. Pièces jointes sont toujours transmis avec le message.
  
Un message qui est transmis a un ou plusieurs destinataires (adresses qui sont associés à un système de messagerie particulier). Certains destinataires sont entrées dans un conteneur qui appartient à un fournisseur de carnet d’adresses dans le profil actuel ; autres destinataires sont créées uniquement pour transmettre le message. Étant donné que les destinataires et les pièces jointes doivent être accessible via le message auxquels ils sont associés, les destinataires et les pièces jointes d’un message sont appelés ses sous-objets. 
  
Fournisseurs de banque de messages prennent en charge les messages, les pièces jointes et les destinataires par le biais de méthodes dans trois interfaces : 
  
|**Interface**|**Description**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Gère les pièces jointes et les destinataires, envoie des messages, définit l’état de lecture.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crée, copie, déplace les messages et les sous-dossiers et gère l’état du message.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Gère les propriétés de la pièce jointe.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

