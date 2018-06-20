---
title: Types de Tables
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 36456c6226b2eb74b8f15995ad0925381302523a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787391"
---
# <a name="types-of-tables"></a>Types de Tables

  
  
**S’applique à**: Outlook 
  
Il existe de nombreux types de tables, chaque type identifié par les informations affichées. Tables activer les applications clientes et des fournisseurs de services pour accéder rapidement et de manipuler les propriétés importantes de nombreux types d’objets. 
  
Certaines tables, telles que les tables des matières, fournissent un autre moyen d’accès aux propriétés. Par exemple, un client peut extraire l’objet d’un message, sa propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), que ce soit directement par le message en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ou par le biais de table des matières du message. Autres tableaux fournissent le seul moyen pour les propriétés de l’objet access. Par exemple, un client ne peut pas accéder à propriété de **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) d’une pièce jointe en appelant **IMAPIProp::GetProps**; Il doit toujours récupérer la table des pièces jointes du message à laquelle il est joint. **PR_ATTACH_METHOD** colonne est obligatoire dans toutes les tables des pièces jointes. 
  
Vue d’une table peut être statiques ou dynamiques. Avec une vue table statique, les modifications apportées aux données sous-jacentes ne provoquent pas l’affichage à mettre à jour. Une fois que l’affichage a été instancié, il ne change pas. Les utilisateurs de tables statiques peuvent être informés des modifications de données via les notifications du tableau. Un affichage de tableau dynamique est mis à jour lorsque des modifications sont apportées aux données. Il existe deux types de tableaux dynamiques : qui met à jour les colonnes de chaque ligne, mais les lignes restent statiques et celle qui met à jour des colonnes et des lignes. Ce type de table ce dernier reflète toujours exactement les données sous-jacentes.
  
Tables ont une colonne par défaut défini, l’ensemble minimal de colonnes un client ou fournisseur de services peut s’attendre lors de la récupération des lignes d’une table qui n’a pas encore été affecté à un [IMAPITable::SetColumns](imapitable-setcolumns.md) appel. Clients et fournisseurs de services peuvent ajouter ou supprimer des colonnes à partir de cette valeur par défaut définie par l’appel de la méthode **SetColumns** . Modifications peuvent être effectuées statiques ou dynamiques, suite à une demande client. Toutes les tables ne prend en charge la modification du jeu de colonne dynamique. 
  
Les tableaux MAPI et leurs implémenteurs et les utilisateurs sont les suivants :
  
|**Table**|**Implémentation**|
|:-----|:-----|
|Pièce jointe  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par les clients et des fournisseurs de transport.  <br/> |
|Contenu  <br/> |Implémentée par message stocker et fournisseurs de carnet d’adresses. Utilisé par les clients.  <br/> |
|Affichage  <br/> |Implémentés par MAPI et fournisseurs de services. Utilisé par MAPI et fournisseurs de services.  <br/> |
|Hiérarchie  <br/> |Implémentée par message stocker et fournisseurs de carnet d’adresses. Utilisé par les clients.  <br/> |
|Service de message  <br/> |Implémentés par MAPI. Utilisé par les clients.  <br/> |
|Banque de messages  <br/> |Implémentés par MAPI. Utilisé par les clients.  <br/> |
|Unique  <br/> |Implémentée par les fournisseurs de carnet d’adresses. Utilisé par MAPI.  <br/> |
|File d’attente sortante  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par le spouleur MAPI.  <br/> |
|Profil  <br/> |Implémentés par MAPI. Utilisé par les clients.  <br/> |
|Provider  <br/> |Implémentés par MAPI. Utilisé par les clients.  <br/> |
|Dossier de r�ception  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par les clients.  <br/> |
|Destinataire  <br/> |Implémenté par les fournisseurs de banque de messages. Utilisé par les clients et des fournisseurs de transport.  <br/> |
|État  <br/> |Implémentés par MAPI et fournisseurs de services. Utilisé par les clients.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

