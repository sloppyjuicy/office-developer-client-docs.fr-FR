---
title: IMAPISupport IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dcd7820e0aab91c0e2ebb23860cc93367f4d552d
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63722875"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des implémentations pour les tâches généralement effectuées par les fournisseurs de services et les fonctions de point d’entrée du service de messagerie. Les fournisseurs de services reçoivent un pointeur vers leur objet de support lorsque MAPI appelle la méthode d’accès de l’objet fournisseur. Les services de message reçoivent leur pointeur d’objet de support dans l’appel à leur fonction de point d’entrée.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets de prise en charge  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISup  <br/> |
|Type de pointeur :  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description|
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente de l’objet de support. |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Récupère les adresses des fonctions d’allocation et de désallocation de mémoire MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md) et [MAPIFreeBuffer](mapifreebuffer.md)). |
|[Subscribe](imapisupport-subscribe.md) <br/> |Inscrit un réception de notification pour recevoir des notifications via MAPI. |
|[Se désabonner](imapisupport-unsubscribe.md) <br/> |Annule la responsabilité de l’envoi de notifications précédemment établies avec un appel à la **méthode Subscribe** . |
|[Notification](imapisupport-notify.md) <br/> |Envoie une notification d’un événement spécifié à une source de conseil qui s’est inscrite à l’origine pour la notification via la **méthode Subscribe** . |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifie le tableau d’état en ajoutant une nouvelle ligne ou en modifiant une ligne existante. |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Inscrit la fonction de préprocesseur d’un fournisseur de transport (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ). |
|[NewUID](imapisupport-newuid.md) <br/> |Crée une structure [MAPIUID](mapiuid.md) à utiliser comme identificateur unique. |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marque un objet comme inutilisable. |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Donne le contrôle de l’UC aupooler MAPI afin qu’il puisse effectuer toutes les tâches qu’il considère nécessaires. |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Avertit lepooler MAPI d’un changement d’état ou d’une demande de service. |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crée un identificateur d’entrée pour une adresse unique. |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Inscrit une structure **MAPIUID** qui représente de manière unique le fournisseur de services. |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Ouvre une entrée de destinataire dans un fournisseur de carnet d’adresses étranger. |
|[OpenEntry](imapisupport-openentry.md) <br/> |Ouvre un objet et renvoie un pointeur d’interface pour un accès supplémentaire. |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Renvoie un pointeur vers le tableau unique MAPI (liste de modèles que tous les fournisseurs de carnet d’adresses peuvent prendre en charge pour la création de destinataires). |
|[Address](imapisupport-address.md) <br/> |Affiche la boîte de dialogue Adresse commune. |
|[Détails](imapisupport-details.md) <br/> |Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière. |
|[NewEntry](imapisupport-newentry.md) <br/> |Ajoute un nouveau destinataire directement à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant. |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Affiche une feuille des propriétés de configuration. |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copie ou déplace des messages d’un dossier vers un autre dossier. |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copie ou déplace un dossier de son dossier parent actuel vers un autre dossier parent. |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copie ou déplace toutes les propriétés d’un objet, à l’exception des propriétés spécifiquement exclues, vers un autre objet. |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copie ou déplace une ou plusieurs propriétés d’un objet vers un autre objet. |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Récupère un objet de progression qui affiche un indicateur de progression. |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Génère un rapport en lecture ou non lu pour un message. |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prépare un message à envoyer aupooler MAPI. |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Complète la liste des destinataires d’un message, en développe des listes de distribution particulières. |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Traite un message envoy�. |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Permet d’accéder au carnet d’adresses. |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Effectue un post-traitement sur un message. |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Demande la publication ordonnée d’une boutique de messages. |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Génère des rapports de remise et de non remise. |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Convertit l’identificateur d’entrée interne d’une boutique de messages en identificateur d’entrée au format mapi standard. |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Modifie définitivement une section de profil de magasin de messages. |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implémente un objet de stockage pour accéder à un flux. |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crée un objet de support de service de message. |
   
## <a name="remarks"></a>Remarques

Les carnets d’adresses, les magasins de messages, les fournisseurs de transport et les services de messagerie ont chacun leurs propres objets de support. Les fournisseurs de services et les services de messagerie appellent les méthodes dans leurs objets de support dans le cadre de leurs implémentations d’autres méthodes d’interface. Chaque objet de support dispose d’implémentations complètes des méthodes qui s’appliquent à son appelant ; les méthodes qui ne sont pas applicables retournent MAPI_E_NO_SUPPORT. Les objets de support du fournisseur de carnet d’adresses ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |... |
|:-----|:-----|:-----|
|**Address** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Détails** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notification** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Se désabonner** <br/> |**WrapStoreEntryID** <br/> |
   
Les objets de prise en charge du fournisseur de magasins de messages ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |... |
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notification** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Se désabonner** <br/> |
|**WrapStoreEntryID** <br/> |
   
Les objets de prise en charge des fournisseurs de transport ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |... |
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notification** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Se désabonner** <br/> |
   
Les objets de support du service de message ont des implémentations pour les méthodes suivantes :
  
|Méthode |... |
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

