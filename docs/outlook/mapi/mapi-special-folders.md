---
title: Dossiers sp�ciaux MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b55985cb10b708c8c3da20492f96a5a6bc2c690a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584107"
---
# <a name="mapi-special-folders"></a>Dossiers sp�ciaux MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI d�finit quelques dossiers sp�ciaux, car ils traiter les r�les pr�d�finis comme dossiers par d�faut pour certains types de messages. Ces dossiers sp�ciaux ne peut g�n�ralement �tre supprim�s, et ils ont des propri�t�s d'identificateur d'entr�e sp�cial.
  
Il existe huit dossiers sp�ciaux, certains qui font partie de la sous-arborescence message interpersonnel (IPM). MAPI cr�e ces dossiers avant un client re�oit l'acc�s � la base de messages, apr�s lequel le client peut �tre en mesure de supprimer les dossiers, si n�cessaire. Certains fournisseurs de banque de messages autorisent la suppression, tandis que d'autres personnes n'est pas le cas. Le tableau suivant d�crit ces dossiers.
  
**Dossiers MAPI**

|**Dossier**|**Description**|
|:-----|:-----|
|Dossier bo�te d'envoi  <br/> |Contient les messages sortants IPM.  <br/> |
|Dossier �l�ments supprim�s  <br/> |Contient des messages IPM sont marqu�es pour suppression.  <br/> |
|dossier �l�ments envoy�s  <br/> |Contient des messages IPM qui ont �t� envoy�s.  <br/> |
|Dossier racine IPM  <br/> |Contient des dossiers pour la gestion des messages IPM.  <br/> |
|Dossier de r�ception  <br/> |Contient les messages entrants pour une classe de message particulier.  <br/> |
|Dossier racine de r�sultats de recherche  <br/> |Contient des dossiers pour la gestion des r�sultats de recherche.  <br/> |
|Dossier racine de commun-vues  <br/> |Contient des dossiers pour la gestion des affichages pour la banque de messages.  <br/> |
|Dossier racine de personnel-vues  <br/> |Contient des dossiers pour la gestion des vues pour un utilisateur particulier.  <br/> |
   
The first four folders relate to the IPM subtree, a tree of folders that MAPI creates when a message store is initialized. Default message stores for interactive messaging clients always include the IPM folder subtree and the other special folders in their folder hierarchy. Non-default message stores are required only to support the search-results root folder, the IPM subtree root folder, the Deleted Items folder, and the receive folder. To ensure that the IPM subtree folders exist and are valid, clients can call the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. **HrValidateIPMSubtree** checks the folders and recreates them if there is a problem. 
  
Les dossiers racine pour les r�sultats de recherche, commune et des affichages personnels ne font pas partie de la sous-arborescence IPM ; ces dossiers sont cr��s dans le dossier racine de la banque de messages. Le dossier racine de r�sultats de recherche contient des dossiers qui prennent en charge les tables des mati�res avec les messages qui r�pondent � un ensemble de crit�res de recherche. Bien que les clients sont autoris�s � cr�er des dossiers de r�sultats de recherche dans n'importe quel dossier, la plupart des clients d�signer un dossier racine unique pour �tre le parent de tous les r�sultats de recherche les dossiers cr��s au cours de la session. 
  
Les dossiers racine commun-vues et personnel-vues contiennent des messages qui d�crivent des vues ou des m�thodes conseill�es de pr�senter les donn�es de message et le dossier. Le dossier racine commun-vues contient les affichages que les clients peuvent utiliser avec n'importe quel dossier dans la banque de messages ; le dossier personnel-vues contient des vues qui ont �t� d�finis par un utilisateur sp�cifique pour un ou plusieurs dossiers particulier.
  
Les clients qui fonctionnent avec les messages IPM doivent cr�er tous les dossiers et messages sous le dossier racine de la sous-arborescence IPM, plut�t que dans le dossier racine de la banque de messages. Ainsi, les clients non-IPM � les clients qui g�rent les messages �chang�s entre les ordinateurs ou entre l'homme et les ordinateurs � un moyen facile de masquer leurs messages � partir de clients IPM. 
  
MAPI assigns special entry identifier properties for these special folders. For a list of the special folder entry identifiers, see [Ouverture d'un dossier de la banque de messages](opening-a-message-store-folder.md).
  
### <a name="outlook-special-folders"></a>Dossiers sp�ciaux Outlook

Dossiers sp�ciaux Outlook sont identifi�s par leur identificateurs qui sont stock�s dans le dossier bo�te de r�ception et le dossier racine de la banque de messages d'entr�e.
  
|**Folder**|**La propri�t� � d�finir**|
|:-----|:-----|
|Calendrier  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Contacts  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Journal  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Remarques  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Tâches  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
|Brouillons  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

