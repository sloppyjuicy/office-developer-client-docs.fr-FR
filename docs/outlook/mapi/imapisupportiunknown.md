---
title: IMAPISupport IUnknown
description: IMAPISupportIUnknown fournit des implémentations pour les tâches qui sont généralement effectuées par les fournisseurs de services et les fonctions de point d’entrée du service de message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
ms.openlocfilehash: 5e3a06ac1fb3e55f979cff7fb47dab151b6459c1
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827890"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des implémentations pour les tâches qui sont généralement effectuées par les fournisseurs de services et les fonctions de point d’entrée du service de message. Les fournisseurs de services reçoivent un pointeur vers leur objet de support lorsque MAPI appelle la méthode d’ouverture de session de l’objet fournisseur. Les services de message reçoivent leur pointeur d’objet de support dans l’appel à leur fonction de point d’entrée.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets de prise en charge  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISup  <br/> |
|Type de pointeur :  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description|
|:-----|:-----|
|[Getlasterror](imapisupport-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur d’objet de support précédente. |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Récupère les adresses des fonctions d’allocation et de désallocation de mémoire MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md) et [MAPIFreeBuffer](mapifreebuffer.md)). |
|[Subscribe](imapisupport-subscribe.md) <br/> |Inscrit un récepteur de conseils pour recevoir des notifications via MAPI. |
|[Se désabonner](imapisupport-unsubscribe.md) <br/> |Annule la responsabilité de l’envoi de notifications précédemment établies avec un appel à la méthode **Subscribe** . |
|[Notification](imapisupport-notify.md) <br/> |Envoie une notification d’un événement spécifié à une source de conseil qui s’est inscrite à l’origine pour la notification par le biais de la méthode **Subscribe** . |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifie la table d’état en ajoutant une nouvelle ligne ou en modifiant une ligne existante. |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Inscrit la fonction de préprocesseur d’un fournisseur de transport (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ). |
|[NewUID](imapisupport-newuid.md) <br/> |Crée une structure [MAPIUID](mapiuid.md) à utiliser comme identificateur unique. |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marque un objet comme inutilisable. |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Donne le contrôle de l’UC au spouleur MAPI afin qu’il puisse effectuer toutes les tâches qu’il juge nécessaires. |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifie le spouleur MAPI d’un changement d’état ou d’une demande de service. |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crée un identificateur d’entrée pour une adresse unique. |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Inscrit une structure **MAPIUID** qui représente de façon unique le fournisseur de services. |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Ouvre une entrée de destinataire dans un fournisseur de carnet d’adresses étranger. |
|[OpenEntry](imapisupport-openentry.md) <br/> |Ouvre un objet et retourne un pointeur d’interface pour un accès supplémentaire. |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Retourne un pointeur vers la table unique MAPI (liste de modèles pris en charge par tous les fournisseurs de carnets d’adresses pour la création de nouveaux destinataires). |
|[Adresse](imapisupport-address.md) <br/> |Affiche la boîte de dialogue d’adresse commune. |
|[Détails](imapisupport-details.md) <br/> |Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière. |
|[NewEntry](imapisupport-newentry.md) <br/> |Ajoute un nouveau destinataire directement à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant. |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Affiche une feuille de propriétés de configuration. |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copie ou déplace les messages d’un dossier vers un autre dossier. |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copie ou déplace un dossier de son dossier parent actuel vers un autre dossier parent. |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copie ou déplace toutes les propriétés d’un objet, à l’exception des propriétés spécifiquement exclues, vers un autre objet. |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copie ou déplace une ou plusieurs propriétés d’un objet vers un autre objet. |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Récupère un objet de progression qui affiche un indicateur de progression. |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Génère un rapport lu ou non lu pour un message. |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prépare un message pour l’envoi au spouleur MAPI. |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Termine la liste des destinataires d’un message, en développant des listes de distribution particulières. |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Traite un message envoy�. |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Fournit l’accès au carnet d’adresses. |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Effectue une post-traitement sur un message. |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Demande la publication ordonnée d’un magasin de messages. |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Génère des rapports de remise et non remis. |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Convertit l’identificateur d’entrée interne d’un magasin de messages en identificateur d’entrée au format standard MAPI. |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Rend permanentes les modifications apportées à une section de profil de magasin de messages. |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implémente un objet de stockage pour accéder à un flux. |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crée un objet de support de service de message. |
   
## <a name="remarks"></a>Remarques

Les carnets d’adresses, les magasins de messages, les fournisseurs de transport et les services de messages ont chacun leurs propres objets de support. Les fournisseurs de services et les services de messages appellent les méthodes dans leurs objets de support dans le cadre de leurs implémentations d’autres méthodes d’interface. Chaque objet de support a des implémentations complètes des méthodes qui s’appliquent à son appelant ; les méthodes qui ne sont pas applicables retournent MAPI_E_NO_SUPPORT. Les objets de prise en charge du fournisseur de carnet d’adresses ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |... |
|:-----|:-----|:-----|
|**Adresse** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Détails** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**Getlasterror** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notification** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Se désabonner** <br/> |**WrapStoreEntryID** <br/> |
   
Les objets de prise en charge du fournisseur du magasin de messages ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |... |
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**Getlasterror** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notification** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Se désabonner** <br/> |
|**WrapStoreEntryID** <br/> |
   
Les objets de prise en charge du fournisseur de transport ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |... |
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**Getlasterror** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notification** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Se désabonner** <br/> |
   
Les objets de prise en charge du service de message ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**Getlasterror** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

