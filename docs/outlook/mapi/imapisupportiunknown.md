---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4843a52d7441de1e1ab545e80346db8dd308c4bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590203"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit des implémentations pour les tâches qui sont généralement effectuées par les fournisseurs de services et fonctions de point d’entrée message service. Fournisseurs de services s’affiche un pointeur vers l’objet de prise en charge MAPI appelle la méthode d’ouverture de session de l’objet de leur fournisseur. Services de messagerie reçoivent le pointeur d’objet de prise en charge dans l’appel de fonction de leur point d’entrée.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposés par :  <br/> |Prise en charge des objets  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPISup  <br/> |
|Type de pointeur :  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur d’objet prise en charge précédente.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Récupère les adresses des mémoire allocation et libération de fonctions MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Enregistre un récepteur de notifications pour recevoir des notifications par le biais de MAPI.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Annule la responsabilité de l’envoi de notifications précédemment établie par un appel à la méthode **Subscribe** .  <br/> |
|[Avertir](imapisupport-notify.md) <br/> |Envoie une notification d’un événement spécifié à une source d’advise initialement enregistré pour la notification par le biais de la méthode **Subscribe** .  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifie la table d’état en ajoutant une nouvelle ligne ou de modification d’une ligne existante.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Enregistre la fonction préprocesseur d’un fournisseur de transport (une fonction qui est conforme au prototype [PreprocessMessage](preprocessmessage.md) ).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Crée une nouvelle structure [MAPIUID](mapiuid.md) pour être utilisé comme un identificateur unique.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marque un objet comme étant inutilisable.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Donne le contrôle de l’UC pour le spouleur MAPI afin qu’elle puisse exécuter toutes les tâches qu’elle estime nécessaires.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifie le spouleur MAPI d’un changement de statut ou une demande de service.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crée un identificateur d’entrée pour une adresse unique.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Enregistre une structure **MAPIUID** qui représente le fournisseur de services de manière unique.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Ouvre une entrée de destinataires dans un fournisseur de carnet d’adresse étrangère.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Ouvre un objet et retourne un pointeur d’interface pour l’accès des autres.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Retourne un pointeur vers le tableau unique de MAPI (une liste des modèles que tous les du carnet d’adresses fournisseurs de prise en charge pour la création de nouveaux destinataires).  <br/> |
|[Adresse](imapisupport-address.md) <br/> |Affiche la boîte de dialogue adresses.  <br/> |
|[Détails](imapisupport-details.md) <br/> |Affiche une boîte de dialogue qui affiche des informations sur une entrée de carnet d’adresses particulière.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Ajoute un nouveau destinataire directement à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Affiche une feuille de propriétés de configuration.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copie ou déplace les messages d’un dossier dans un autre dossier.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copie ou déplace un dossier à partir de son dossier parent en cours vers un autre dossier parent.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copie ou déplace toutes les propriétés d’un objet, à l’exception des propriétés exclues en particulier, à un autre objet.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copie ou déplace une ou plusieurs propriétés d’un objet à un autre objet.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Récupère un objet de progression qui affiche un indicateur de progression.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Génère un rapport nonread pour un message ou en lecture.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Il prépare un message pour son envoi au spouleur MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Termine la liste des destinataires d’un message, développer des listes de distribution particulier.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Traite un message envoy�.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Fournit l’accès au carnet d’adresses.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Effectue post-traitement sur un message.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Demande la version ordonnée d’une banque de messages.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Génère des rapports de remise et de non-remise.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Convertit un identificateur d’entrée dans le format standard MAPI identificateur d’entrée interne d’une banque de messages.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Modifie un message stocker la section profil définitive.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implémente un objet de stockage pour accéder à un objet stream.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crée un objet de prise en charge de service de message.  <br/> |
   
## <a name="remarks"></a>Remarques

Carnets d’adresses, les banques de messages, les fournisseurs de transport et message services chaque ont leurs propres objets de prise en charge. Fournisseurs de services et les services de messagerie appellent les méthodes dans leurs objets de prise en charge dans le cadre de leurs implémentations des méthodes d’interface. Chaque objet de prise en charge différentes a terminé implémentations des méthodes qui s’appliquent à l’appelant ; les méthodes qui ne sont pas applicables retournent MAPI_E_NO_SUPPORT. Objets de prise en charge adresse book fournisseur ont des implémentations des méthodes suivantes :
  
||||
|:-----|:-----|:-----|
|**Adresse** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Détails** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Avertir** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Objets de prise en charge du fournisseur de magasin de message ont des implémentations des méthodes suivantes :
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Avertir** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Prise en charge des objets du fournisseur de transport ont des implémentations des méthodes suivantes :
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Avertir** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
   
Objets de prise en charge de service de message ont des implémentations des méthodes suivantes :
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

