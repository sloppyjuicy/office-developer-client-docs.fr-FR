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
ms.openlocfilehash: 10e49875b1a63b58b318c80ce1c9cb2c985c5c88
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773585"
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
|[OpenEntry](iaddrbook-openentry.md) <br/> |Ouvre une entrée de carnet d’adresses et renvoie un pointeur vers une interface qui peut être utilisée pour accéder à l’entrée. |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compare deux identificateurs d’entrée appartenant à un fournisseur de carnet d’adresses particulier pour déterminer s’ils font référence au même objet de carnet d’adresses. |
|[Conseiller](iaddrbook-advise.md) <br/> |Enregistre un client ou un fournisseur de services pour recevoir des notifications concernant les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses. |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses. |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Crée un identificateur d’entrée pour une adresse unique. |
|[NewEntry](iaddrbook-newentry.md) <br/> |Ajoute un nouveau destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant. |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Effectue la résolution de noms, en attribuant des identificateurs d’entrée aux destinataires d’une liste de destinataires. |
|[Address](iaddrbook-address.md) <br/> |Affiche la boîte de dialogue Outlook carnet d’adresses. |
|[Détails](iaddrbook-details.md) <br/> |Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière. |
|**RecipOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Renvoie l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel . |
|[SetPAB](iaddrbook-setpab.md) <br/> |Désigne un conteneur particulier en tant que carnet d’adresses personnel (PAB). |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initial. |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Établit le conteneur spécifié en tant que conteneur de carnet d’adresses par défaut initialement disponible. |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Renvoie une liste ordonnée d’identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la [méthode ResolveName](iaddrbook-resolvename.md) . |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Définit un nouveau chemin de recherche dans le profil utilisé pour le processus de résolution de noms. |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

