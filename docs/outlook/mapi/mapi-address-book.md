---
title: Carnet d'adresses MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b328a65f400e424fb2cd177e710fb8bcffa392c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784551"
---
# <a name="mapi-address-book"></a>Carnet d'adresses MAPI

  
  
**S’applique à**: Outlook 
  
Le carnet d'adresses int�gr� est un objet qui impl�mente la MAPI pour fournir l'acc�s � une collection int�gr�e d'informations sur les adresses de tous les fournisseurs de carnet d'adresses dans le profil. Avec le carnet d'adresses, les fournisseurs de services et les applications clientes n'ont pas faire la distinction entre les mod�les d'adressage uniques des syst�mes de messagerie. Au lieu de cela, ils peuvent consulter les adresses des destinataires dans n'importe quel syst�me de messagerie, dans la mesure o� le fournisseur de carnet d'adresses pour le syst�me de messagerie est install�.
  
Le carnet d'adresses sont accessibles par programmation, sans l'intervention de l'utilisateur, ou de mani�re interactive � l'aide des bo�tes de dialogue courantes. MAPI inclut des bo�tes de dialogue pour afficher une liste r�capitulative des entr�es dans le carnet d'adresses, des informations d�taill�es sur un destinataire particulier, un avertissement lorsqu'un utilisateur cr�e un destinataire qui ne peuvent pas �tre mapp� � une adresse unique et des formulaires de mod�le pour la cr�ation de nouveaux destinataires.
  
Le carnet d'adresses MAPI est une structure semblable � une banque de messages dans la mesure o� elle est organis� de mani�re hi�rarchique. Le carnet d'adresses fournit l'acc�s aux trois types d'objets impl�ment�s par un fournisseur de carnet d'adresses :
  
- Un objet conteneur de carnet d'adresses.
    
- Un objet de liste de distribution.
    
- Un objet utilisateur de messagerie.
    
Chacun de ces types d'objets est accessible par le biais de son identificateur d'entr�e unique qui est affect� par son fournisseur de carnet d'adresses. 
  
Conteneurs de carnet d'adresses sont similaires aux dossiers en ce sens qu'ils contiennent des objets de diff�rents types. Un conteneur de carnet d'adresses peut contenir autres conteneurs de carnet d'adresses, ainsi que la messagerie des objets utilisateur et de la distribution de la liste. Conteneurs de carnet d'adresses sont utilis�s pour organiser et stocker des objets de carnet d'adresses.
  
Pour obtenir l'apparence int�gr�e du carnet d'adresses, fournisseurs de carnet d'adresses exposent z�ro, un ou plusieurs de leurs conteneurs de niveau sup�rieur � MAPI qui les fusionne et affiche les r�sultats dans un conteneur de niveau sup�rieur unique. Fournisseurs de carnet d'adresses peuvent choisir d'exposer un ensemble de conteneurs pour un seul type de session et un ensemble diff�rent de la messagerie pour une autre session. Il est �galement possible, pour les fournisseurs de carnet d'adresses n'ont aucun conteneur de niveau sup�rieur et d'exposer uniquement une liste de mod�les qui peuvent servir � cr�er des destinataires.
  
Destinataires du message sont impl�ment�es � l'utilisateur de messagerie et les objets de liste de distribution. Les utilisateurs de messagerie sont des destinataires individuels ; listes de distribution sont les destinataires de groupe. Chaque utilisateur de messagerie poss�de une adresse unique d'un type particulier g�r� par un syst�me de messagerie sp�cifique. Une liste de distribution est un ensemble nomm� de destinataires. Listes de distribution peuvent contenir les objets utilisateur de messagerie et d'autres listes de distribution. Lorsqu'un utilisateur d'une application cliente envoie un message � une liste de distribution, le message est envoy� � chacun des membres d'utilisateurs de messagerie de la liste. 
  
Les listes de distribution et les utilisateurs de messagerie ont un ensemble de cinq propri�t�s appel�es les propri�t�s de l'adresse de base. Ces propri�t�s requises et sont d�crites bri�vement comme suit.
  
|**Propri�t� de l'adresse de base**|**Description**|
|:-----|:-----|
|**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Type d'adresse du destinataire. Chaque type d'adresse respecte un format sp�cifique et est utilis� avec un syst�me de messagerie sp�cifique.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Nom affichable pour le destinataire.  <br/> |
|**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Adresse du destinataire.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Identificateur d'entr�e permettant d'acc�der au destinataire.  <br/> |
|**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Touche comparable binaire utilis� pour identifier le destinataire.  <br/> |
   
MAPI d�finit le nombre de groupes de propri�t�s qui sont des variantes des propri�t�s de l'adresse de base. Ces autres groupes d�crivent des utilisateurs de messagerie et des listes de distribution dans des situations diff�rentes. Par exemple, un groupe de propri�t�s d�crit l'exp�diteur de d�l�gu� d'un message et un autre groupe le destinataire de d�l�gu�.
  

