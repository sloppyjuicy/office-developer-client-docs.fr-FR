---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3d78b4e6a4a0cc3363edefc84e7ae80dbe72c510
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590357"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de point d’entrée de service fournisseur qui appelle de l’Assistant profil pour récupérer suffisamment d’informations pour afficher les feuilles de propriétés de configuration du fournisseur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz.h  <br/> |
|Fonction implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |Assistant profil MAPI  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Paramètres

 _hProviderDLLInstance_
  
> [in] Descripteur d’instances de la DLL du fournisseur de services. 
    
 _lpcsResourceName_
  
> [out] Pointeur vers une chaîne qui contient le nom complet de la ressource de la boîte de dialogue qui doit être affichée par l’Assistant profil lors de la configuration. La taille maximale de la chaîne, y compris le terminateur NULL, est de 32 caractères. 
    
 _lppDlgProc_
  
> [out] Pointeur vers une procédure de boîte de dialogue Windows standard qui sera appelée par l’Assistant profil pour notifier le fournisseur d’événements différents. 
    
 _lpMAPIProp_
  
> [in] Pointeur vers une implémentation d’interface de propriété qui fournit l’accès aux propriétés de configuration. 
    
 _lpMapiSupportObject_
  
> [in] Pointeur vers l’objet de prise en charge MAPI applicable à cette session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Fonction **WIZARDENTRY** du fournisseur de services a été appelée avec succès. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

L’Assistant profil appelle la fonction **WIZARDENTRY** en fonction de lorsque celle-ci est prête afficher l’interface utilisateur de configuration du fournisseur de services. Lorsque l’Assistant profil est terminé de configurer tous les fournisseurs, il écrit les propriétés de configuration dans le profil en appelant [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Le nom de la fonction **WIZARDENTRY** en fonction de doit être placé dans l’entrée WIZARD_ENTRY_NAME MAPISVC.INF. 
  
Le nom de la ressource est que de la ressource de la boîte de dialogue qui sera affiché dans le volet de l’Assistant profil. La ressource est passée arrière doit contenir toutes les pages dans une ressource de la boîte de dialogue unique. Lorsque l’Assistant profil reçoit cette ressource, il ignore le style de la boîte de dialogue, mais pas les styles du contrôle et crée tous les contrôles enfants de la page Assistant profil. Tous les contrôles sont masqués à l’origine. Fournisseurs doivent s’assurer que les coordonnées de leurs contrôles sont zéro ou en partant de zéro, et qu’elles ne dépassent pas une largeur maximale de 200 unités de la boîte de dialogue et une hauteur maximale de 150 unités de boîte de dialogue. Identificateurs de contrôle ci-dessous 400 sont réservés à l’Assistant profil. L’Assistant profil affiche le titre du fournisseur en gras au-dessus de l’interface du fournisseur utilisateur. 
  
Le pointeur d’interface de propriété fourni dans le paramètre _lpMAPIProp_ doit être conservé par le fournisseur pour référence ultérieure. Traite uniquement l’ensemble plus élémentaire des propriétés de l’Assistant profil et le fournisseur peut utiliser l’implémentation d’interface de propriété pour inclure les propriétés supplémentaires. Pendant la configuration, les fournisseurs doivent ajouter leurs propriétés de configuration à l’objet qui implémente l’interface de la propriété. Une fois que tous les fournisseurs ont été configurés, l’Assistant profil ajoute ces propriétés dans le profil. 
  
Pour plus d’informations sur l’utilisation de cette fonction, voir [Configuration du Service de Message prise en charge](supporting-message-service-configuration.md). 
  

