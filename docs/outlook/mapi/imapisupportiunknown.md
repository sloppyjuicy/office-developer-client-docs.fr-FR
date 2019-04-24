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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325647"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des implémentations pour les tâches généralement effectuées par des fournisseurs de services et des fonctions de point d'entrée de service de message. Les fournisseurs de services reçoivent un pointeur vers leur objet de prise en charge lorsque MAPI appelle la méthode d'ouverture de session de l'objet fournisseur. Les services de messagerie reçoivent leur pointeur d'objet de prise en charge dans l'appel à leur fonction de point d'entrée.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Exposé par:  <br/> |Objets de prise en charge  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPISup  <br/> |
|Type de pointeur:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](imapisupport-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur de l'objet de prise en charge précédent.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Récupère les adresses des fonctions d'allocation et de désallocation de mémoire MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Abonné](imapisupport-subscribe.md) <br/> |Enregistre un récepteur de notifications pour recevoir des notifications via MAPI.  <br/> |
|[Se désabonner](imapisupport-unsubscribe.md) <br/> |Annule la responsabilité pour l'envoi de notifications précédemment établies avec un appel à la méthode **subscribe** .  <br/> |
|[Avertir](imapisupport-notify.md) <br/> |Envoie une notification d'un événement spécifié à une source de notification qui a été initialement inscrite pour la notification par le biais de la méthode **subscribe** .  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifie la table d'État en ajoutant une nouvelle ligne ou en modifiant une ligne existante.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Ouvre une section du profil actif et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Enregistre la fonction de préprocesseur d'un fournisseur de transport (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Crée une nouvelle structure [MAPIUID](mapiuid.md) à utiliser comme identificateur unique.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marque un objet comme inutilisable.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Donne le contrôle de l'UC au spouleur MAPI afin qu'il puisse effectuer toutes les tâches qu'il juge nécessaires.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Avertit le spouleur MAPI de la modification de l'État ou d'une demande de service.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crée un identificateur d'entrée pour une adresse ponctuelle.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Inscrit une structure **MAPIUID** qui représente le fournisseur de services de manière unique.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Ouvre une entrée de destinataire dans un fournisseur de carnets d'adresses étrangers.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Ouvre un objet et renvoie un pointeur d'interface pour un accès supplémentaire.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Renvoie un pointeur vers la table ponctuelle MAPI (une liste de modèles que tous les fournisseurs de carnet d'adresses prennent en charge pour la création de destinataires).  <br/> |
|[Address](imapisupport-address.md) <br/> |Affiche la boîte de dialogue adresse commune.  <br/> |
|[Details](imapisupport-details.md) <br/> |Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d'adresses particulière.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Ajoute un nouveau destinataire directement à un conteneur de carnet d'adresses ou à la liste des destinataires d'un message sortant.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Affiche une feuille de propriétés de configuration.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copie ou déplace les messages d'un dossier vers un autre dossier.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copie ou déplace un dossier à partir de son dossier parent actuel vers un autre dossier parent.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copie ou déplace toutes les propriétés d'un objet, à l'exception des propriétés spécifiquement exclues, vers un autre objet.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copie ou déplace une ou plusieurs propriétés d'un objet vers un autre objet.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Récupère un objet de progression qui affiche un indicateur de progression.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Génère un rapport de lecture ou de non-lecture pour un message.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prépare un message à envoyer au spouleur MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Complète la liste de destinataires d'un message, en développant des listes de distribution particulières.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Traite un message envoy�.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Permet d'accéder au carnet d'adresses.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Effectue un post-traitement sur un message.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Demande le lancement ordonné d'une banque de messages.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Génère des rapports de remise et de livraison.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |ConVertit l'identificateur d'entrée interne d'une banque de messages en un identificateur d'entrée au format MAPI standard.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Apporte des modifications permanentes à une section de profil de banque de messages.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implémente un objet de stockage pour accéder à un flux.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crée un objet de prise en charge du service de messagerie.  <br/> |
   
## <a name="remarks"></a>Remarques

Les carnets d'adresses, les banques de messages, les fournisseurs de transport et les services de messagerie disposent chacun de leurs propres objets de prise en charge. Les services de messagerie et les fournisseurs de services appellent les méthodes dans leurs objets de prise en charge dans le cadre de leurs implémentations d'autres méthodes d'interface. Chaque objet de prise en charge est doté de toutes les implémentations des méthodes qui s'appliquent à son appelant; les méthodes qui ne sont pas applicables retournent MAPI_E_NO_SUPPORT. Les objets de prise en charge du fournisseur de carnets d'adresses comportent des implémentations pour les méthodes suivantes:
  
||||
|:-----|:-----|:-----|
|**Address** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Details** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**Généré** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Avertir** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Abonné** <br/> |**Se désabonner** <br/> |**WrapStoreEntryID** <br/> |
   
Les objets de prise en charge du fournisseur de banque de messages comportent des implémentations pour les méthodes suivantes:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**Généré** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Avertir** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Abonné** <br/> |**Se désabonner** <br/> |
|**WrapStoreEntryID** <br/> |
   
Les objets de prise en charge de fournisseur de transport ont des implémentations pour les méthodes suivantes:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**Généré** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Avertir** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Abonné** <br/> |**Se désabonner** <br/> |
   
Les objets de prise en charge du service de messagerie comportent des implémentations pour les méthodes suivantes:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**Généré** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

