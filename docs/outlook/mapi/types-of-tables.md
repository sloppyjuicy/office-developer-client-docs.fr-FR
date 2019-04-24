---
title: Types de tables
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 732b3d724c855d978250afff3d05c7f19909a5b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356573"
---
# <a name="types-of-tables"></a>Types de tables

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreux types de tables différents, dont chaque type est différencié par les informations qu'il présente. Les tableaux permettent aux applications clientes et aux fournisseurs de services d'accéder facilement aux propriétés importantes de nombreux types d'objets et de les manipuler. 
  
Certaines tables, comme les tables de contenu, fournissent une autre façon d'accéder aux propriétés. Par exemple, un client peut récupérer l'objet d'un message (sa propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))) directement à partir du message en appelant sa méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ou par le biais de la table des matières du message. D'autres tableaux offrent la seule façon d'accéder aux propriétés de l'objet. Par exemple, un client ne peut pas accéder à la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) d'une pièce jointe en appelant **IMAPIProp:: GetProps**; il doit toujours récupérer la table de pièces jointes du message auquel elle est attachée. **PR_ATTACH_METHOD** est une colonne obligatoire dans toutes les tables de pièces jointes. 
  
Un affichage tableau peut être statique ou dynamique. En mode table statique, les modifications apportées aux données sous-jacentes ne provoquent pas la mise à jour de l'affichage. Une fois l'affichage instancié, il ne change pas. Les utilisateurs de tables statiques peuvent être informés des modifications apportées aux données par le biais de notifications de table. Un affichage de tableau dynamique est mis à jour lorsque des modifications sont apportées aux données. Il existe deux types de tables dynamiques: une qui met à jour les colonnes de chaque ligne, mais les lignes restent statiques et une qui met à jour les colonnes et les lignes. Ce dernier type de tableau reflète toujours les données sous-jacentes exactement.
  
Les tableaux ont un jeu de colonnes par défaut, l'ensemble minimal de colonnes qu'un client ou un fournisseur de services peut s'attendre à voir lors de la récupération de lignes d'une table qui n'a pas encore été affectée par un appel [IMAPITable:: SetColumns](imapitable-setcolumns.md) . Les clients et les fournisseurs de services peuvent ajouter ou supprimer des colonnes de cet ensemble par défaut en appelant la méthode **SetColumns** . Les modifications peuvent être effectuées de façon statique ou dynamique, à la suite d'une demande de client. Toutes les tables ne prennent pas en charge la modification dynamique des jeux de colonnes. 
  
Les tables MAPI et leurs implémenteurs et utilisateurs sont les suivants:
  
|**Table**|**Responsables**|
|:-----|:-----|
|Pièce jointe  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par les clients et les fournisseurs de transport.  <br/> |
|Sommaire  <br/> |Implémenté par le magasin de messages et les fournisseurs de carnets d'adresses. Utilisé par les clients.  <br/> |
|Display  <br/> |Implémenté par MAPI et les fournisseurs de services. Utilisé par les fournisseurs de services et MAPI.  <br/> |
|Hierarchy  <br/> |Implémenté par le magasin de messages et les fournisseurs de carnets d'adresses. Utilisé par les clients.  <br/> |
|Service de messagerie  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Banque de messages  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|One-Off  <br/> |Implémenté par les fournisseurs de carnet d'adresses. Utilisé par MAPI.  <br/> |
|File d'attente sortante  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par le spouleur MAPI.  <br/> |
|Profils  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Fournisseur  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Dossier de r�ception  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par les clients.  <br/> |
|Destinataire  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par les clients et les fournisseurs de transport.  <br/> |
|Statut  <br/> |Implémenté par MAPI et les fournisseurs de services. Utilisé par les clients.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

