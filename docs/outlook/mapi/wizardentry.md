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
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430678"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de point d'entrée du fournisseur de services que l'Assistant Profil appelle pour récupérer suffisamment d'informations pour afficher les feuilles de propriétés de configuration du fournisseur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz. h  <br/> |
|Fonction définie implémentée par:  <br/> |Fournisseurs de services  <br/> |
|Fonction définie appelée par:  <br/> |Assistant Profil MAPI  <br/> |
   
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
  
> dans Handle d'instance de la DLL du fournisseur de services. 
    
 _lpcsResourceName_
  
> remarquer Pointeur vers une chaîne qui contient le nom complet de la ressource de boîte de dialogue qui doit être affichée par l'Assistant Profil lors de la configuration. La taille maximale de la chaîne, y compris la marque de fin NULL, est de 32 caractères. 
    
 _lppDlgProc_
  
> remarquer Pointeur vers une procédure de boîte de dialogue Windows standard appelée par l'Assistant Profil pour informer le fournisseur de divers événements. 
    
 _lpMAPIProp_
  
> dans Pointeur vers une implémentation d'interface de propriété qui fournit l'accès aux propriétés de configuration. 
    
 _lpMapiSupportObject_
  
> dans Pointeur vers l'objet de prise en charge MAPI applicable à cette session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La fonction **WIZARDENTRY** du fournisseur de services a été appelée avec succès. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.
    
## <a name="remarks"></a>Remarques

L'Assistant Profil appelle la fonction basée sur **WIZARDENTRY** lorsqu'elle est prête à afficher l'interface utilisateur de configuration du fournisseur de services. Une fois que l'Assistant Profil a terminé la configuration de tous les fournisseurs, il écrit les propriétés de configuration dans le profil en appelant [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le nom de la fonction basée sur **WIZARDENTRY** doit être placé dans l'entrée WIZARD_ENTRY_NAME dans le fichier MAPISVC. inf. 
  
Le nom de la ressource est celui de la ressource de boîte de dialogue qui sera affichée dans le volet de l'Assistant Profil. La ressource qui est passée doit contenir toutes les pages dans une seule ressource de boîte de dialogue. Lorsque l'Assistant Profil reçoit cette ressource, il ignore le style de la boîte de dialogue, mais pas les styles de contrôle, et crée tous les contrôles en tant qu'enfants de la page de l'Assistant Profil. Tous les contrôles sont initialement masqués. Les fournisseurs doivent s'assurer que les coordonnées de leurs contrôles sont zéro ou de base zéro, et qu'ils ne dépassent pas une largeur maximale de 200 unités de boîte de dialogue et une hauteur maximale de 150 unités de boîte de dialogue. Les identificateurs de contrôle inférieurs à 400 sont réservés à l'Assistant Profil. L'Assistant Profil affiche le titre du fournisseur en texte gras au-dessus de l'interface utilisateur du fournisseur. 
  
Le pointeur d'interface de propriété fourni dans le paramètre _lpMAPIProp_ doit être conservé par le fournisseur pour référence ultérieure. L'Assistant Profil traite uniquement le jeu de propriétés le plus simple et le fournisseur peut utiliser l'implémentation de l'interface de propriétés pour inclure des propriétés supplémentaires. Lors de la configuration, les fournisseurs doivent ajouter leurs propriétés de configuration à l'objet qui implémente l'interface de propriété. Une fois que tous les fournisseurs ont été configurés, l'Assistant Profil ajoute ces propriétés au profil. 
  
Pour plus d'informations sur l'utilisation de cette fonction, voir [prise en charge](supporting-message-service-configuration.md)de la configuration du service de messagerie. 
  

