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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579458"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Prend en charge l’accès au carnet d’adresses MAPI et inclut des opérations, telles que l’affichage des boîtes de dialogue courantes ; conteneurs de l’ouverture, messagerie, les utilisateurs et les listes de distribution ; et la résolution de nom.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Exposés par :  <br/> |Objets de carnet d’adresses  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes, les fournisseurs de services  <br/> |
|Identificateur de l’interface :  <br/> |IID_IAddrBook  <br/> |
|Type de pointeur :  <br/> |LPADRBOOK  <br/> |
|Modèle de transaction :  <br/> |Pas accessible en écriture  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Ouvre une entrée de carnet d’adresses et retourne un pointeur vers une interface qui peut servir à accéder à l’entrée.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compare deux identificateurs d’entrée qui appartiennent à un fournisseur de carnet d’adresse spécifique afin de déterminer si elles font référence à l’objet de carnet d’adresses même.  <br/> |
|[Conseiller](iaddrbook-advise.md) <br/> |Enregistre un fournisseur de service ou client pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.  <br/> |
|[L’avertissement](iaddrbook-unadvise.md) <br/> |Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Crée un identificateur d’entrée pour une adresse unique.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Ajoute un destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Effectue la résolution de noms, affectation d’identificateurs d’entrée aux destinataires dans une liste de destinataires.  <br/> |
|[Adresse](iaddrbook-address.md) <br/> |Affiche la boîte de dialogue de carnet d’adresse Outlook.  <br/> |
|[Détails](iaddrbook-details.md) <br/> |Affiche une boîte de dialogue qui affiche des informations sur une entrée de carnet d’adresses particulière.  <br/> |
|**RecipOptions** <br/> | *Non pris en charge ou documentés.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Non pris en charge ou documentés.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Renvoie l’identificateur d’entrée du conteneur qui est désigné comme le carnet d’adresses personnel (CAP).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Désigne un conteneur spécifique comme le carnet d’adresses personnel (CAP).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initiale.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Définit le conteneur spécifié comme le conteneur de carnet d’adresses par défaut qui est initialement disponible.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Renvoie une liste triée des identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [ResolveName](iaddrbook-resolvename.md) .  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Définit un nouveau chemin d’accès de la recherche dans le profil qui est utilisé pour le processus de résolution de nom.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

