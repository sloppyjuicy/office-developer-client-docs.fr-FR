---
title: Types de tableaux
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6a6fb115d3a3105777b1b0e68595c960df0a92b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566247"
---
# <a name="types-of-tables"></a>Types de tableaux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreux types de tableaux différents, chaque type se différencie par les informations qu’il présente. Les tableaux permettent aux applications clientes et aux fournisseurs de services d’accéder et de manipuler facilement les propriétés importantes de nombreux types d’objets. 
  
Certaines tables, telles que les tables des matières, offrent un autre moyen d’accéder aux propriétés. Par exemple, un client peut récupérer l’objet d’un message ( sa propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) directement à partir du message en appelant sa méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ou via la table des matières du message. D’autres tables offrent le seul moyen d’accéder aux propriétés de l’objet. Par exemple, un client ne peut pas accéder à la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) d’une pièce jointe en appelant **IMAPIProp::GetProps**; Elle doit toujours récupérer la table des pièces jointes du message auquel elle est jointe. **PR_ATTACH_METHOD** est une colonne obligatoire dans toutes les tables de pièces jointes. 
  
Un affichage tableau peut être statique ou dynamique. Avec une vue de table statique, les modifications apportées aux données sous-jacentes n’entraînent pas la mise à jour de l’affichage. Une fois l’affichage ins instantié, il ne change pas. Les utilisateurs de tables statiques peuvent être informés des modifications apportées aux données par le biais de notifications de tableau. Une vue de table dynamique est mise à jour lorsque des modifications sont apportées aux données. Il existe deux types de tableaux dynamiques : un qui met à jour les colonnes de chaque ligne, mais les lignes restent statiques et l’autre qui met à jour les colonnes et les lignes. Ce dernier type de tableau reflète toujours exactement les données sous-jacentes.
  
Les tableaux ont un ensemble de colonnes par défaut, l’ensemble minimal de colonnes qu’un client ou un fournisseur de services peut s’attendre à voir lors de la récupération des lignes d’une table qui n’a pas encore été affectée par un appel [IMAPITable::SetColumns.](imapitable-setcolumns.md) Les clients et les fournisseurs de services peuvent ajouter ou supprimer des colonnes de cet ensemble par défaut en appelant la **méthode SetColumns.** Les modifications peuvent être apportées de manière statique ou dynamique, à la suite d’une demande du client. Tous les tableaux ne sont pas en charge la modification de l’ensemble de colonnes dynamiques. 
  
Les tables MAPI et leurs implémenteurs et utilisateurs sont les suivants :
  
|**Table**|**Implementers**|
|:-----|:-----|
|Pièce jointe  <br/> |Implémenté par les fournisseurs de magasins de messages. Utilisé par les clients et les fournisseurs de transport.  <br/> |
|Sommaire  <br/> |Implémenté par les fournisseurs de magasins de messages et de carnets d’adresses. Utilisé par les clients.  <br/> |
|Afficher  <br/> |Implémenté par MAPI et les fournisseurs de services. Utilisé par MAPI et les fournisseurs de services.  <br/> |
|Hierarchy  <br/> |Implémenté par les fournisseurs de magasins de messages et de carnets d’adresses. Utilisé par les clients.  <br/> |
|Service de message  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Magasin de messages  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Un-off  <br/> |Implémenté par les fournisseurs de carnets d’adresses. Utilisé par MAPI.  <br/> |
|File d’attente sortante  <br/> |Implémenté par les fournisseurs de magasins de messages. Utilisé par lepooler MAPI.  <br/> |
|Profils  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Fournisseur  <br/> |Implémenté par MAPI. Utilisé par les clients.  <br/> |
|Dossier de r�ception  <br/> |Implémenté par les fournisseurs de magasins de messages. Utilisé par les clients.  <br/> |
|Destinataire  <br/> |Implémenté par les fournisseurs de magasins de messages. Utilisé par les clients et les fournisseurs de transport.  <br/> |
|Statut  <br/> |Implémenté par MAPI et les fournisseurs de services. Utilisé par les clients.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

