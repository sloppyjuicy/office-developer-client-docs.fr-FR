---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429823"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l'accès au carnet d'adresses MAPI et inclut des opérations telles que l'affichage de boîtes de dialogue courantes; ouverture des conteneurs, des utilisateurs de messagerie et des listes de distribution; et la résolution de noms.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
|Exposé par:  <br/> |Objets de carnet d'adresses  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IAddrBook  <br/> |
|Type de pointeur:  <br/> |LPADRBOOK  <br/> |
|Modèle de transaction:  <br/> |Non accessible en écriture  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Ouvre une entrée de carnet d'adresses et renvoie un pointeur vers une interface qui peut être utilisée pour accéder à l'entrée.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compare deux identificateurs d'entrée qui appartiennent à un fournisseur de carnets d'adresses particulier pour déterminer s'ils font référence au même objet de carnet d'adresses.  <br/> |
|[Recommander](iaddrbook-advise.md) <br/> |Inscrit un client ou un fournisseur de services pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées du carnet d'adresses.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Annule une inscription aux notifications précédemment établie pour une entrée de carnet d'adresses.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Crée un identificateur d'entrée pour une adresse ponctuelle.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Ajoute un nouveau destinataire à un conteneur de carnet d'adresses ou à la liste des destinataires d'un message sortant.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Effectue une résolution de noms, en affectant des identificateurs d'entrée à des destinataires dans une liste de destinataires.  <br/> |
|[Adresse](iaddrbook-address.md) <br/> |Affiche la boîte de dialogue Carnet d'adresses Outlook.  <br/> |
|[Détails](iaddrbook-details.md) <br/> |Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d'adresses particulière.  <br/> |
|**RecipOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Renvoie l'identificateur d'entrée du conteneur désigné comme carnet d'adresses personnel (PAB).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Désigne un conteneur particulier comme carnet d'adresses personnel (PAB).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Renvoie l'identificateur d'entrée pour le conteneur de carnet d'adresses initial.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Établit le conteneur spécifié en tant que conteneur de carnet d'adresses par défaut qui est mis à la disposition initiale.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Renvoie une liste triée d'identificateurs d'entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [ResolveName](iaddrbook-resolvename.md) .  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Définit un nouveau chemin de recherche dans le profil qui est utilisé pour le processus de résolution de noms.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

