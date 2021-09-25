---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2edbc66be1f2f2ae761677c425616e70b77096d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561550"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’accès au carnet d’adresses MAPI et inclut des opérations telles que l’affichage de boîtes de dialogue courantes ; ouverture de conteneurs, d’utilisateurs de messagerie et de listes de distribution ; et d’effectuer une résolution de nom.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objets de carnet d’adresses  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IAddrBook  <br/> |
|Type de pointeur :  <br/> |LPADRBOOK  <br/> |
|Modèle de transaction :  <br/> |Non accessible en writable  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Ouvre une entrée de carnet d’adresses et renvoie un pointeur vers une interface qui peut être utilisée pour accéder à l’entrée.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compare deux identificateurs d’entrée appartenant à un fournisseur de carnet d’adresses particulier pour déterminer s’ils font référence au même objet de carnet d’adresses.  <br/> |
|[Conseiller](iaddrbook-advise.md) <br/> |Enregistre un client ou un fournisseur de services pour recevoir des notifications concernant les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Crée un identificateur d’entrée pour une adresse unique.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Ajoute un nouveau destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Effectue la résolution de noms, en attribuant des identificateurs d’entrée aux destinataires d’une liste de destinataires.  <br/> |
|[Address](iaddrbook-address.md) <br/> |Affiche la boîte de dialogue Outlook carnet d’adresses.  <br/> |
|[Détails](iaddrbook-details.md) <br/> |Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière.  <br/> |
|**RecipOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Renvoie l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel.  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Désigne un conteneur particulier en tant que carnet d’adresses personnel (PAB).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initial.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Établit le conteneur spécifié en tant que conteneur de carnet d’adresses par défaut initialement disponible.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Renvoie une liste ordonnée d’identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la [méthode ResolveName.](iaddrbook-resolvename.md)  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Définit un nouveau chemin de recherche dans le profil utilisé pour le processus de résolution de noms.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

