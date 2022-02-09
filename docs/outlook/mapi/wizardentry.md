---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a7b237821c2e989e9ef2b9bfdee4668c2d583827
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462805"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de point d’entrée de fournisseur de services que l’Assistant Profil appelle pour récupérer suffisamment d’informations pour afficher les feuilles de propriétés de configuration du fournisseur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz.h  <br/> |
|Fonction définie implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Fonction définie appelée par :  <br/> |Assistant Profil MAPI  <br/> |
   
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
  
> [in] Handle d’instance de la DLL du fournisseur de services. 
    
 _lpcsResourceName_
  
> [out] Pointeur vers une chaîne qui contient le nom complet de la ressource de boîte de dialogue qui doit être affichée par l’Assistant Profil pendant la configuration. La taille maximale de la chaîne, y compris le terminateur NULL, est de 32 caractères. 
    
 _lppDlgProc_
  
> [out] Pointeur vers une procédure Windows boîte de dialogue standard qui sera appelée par l’Assistant Profil pour notifier le fournisseur de divers événements. 
    
 _lpMAPIProp_
  
> [in] Pointeur vers une implémentation d’interface de propriétés qui donne accès aux propriétés de configuration. 
    
 _lpMapiSupportObject_
  
> [in] Pointeur vers l’objet de support MAPI applicable à cette session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La fonction **WIZARDENTRY** du fournisseur de services a été appelée avec succès. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération.
    
## <a name="remarks"></a>Remarques

L’Assistant Profil appelle **la fonction BASÉE SUR WIZARDENTRY** lorsqu’il est prêt à afficher l’interface utilisateur de configuration du fournisseur de services. Lorsque l’Assistant Profil a terminé de configurer tous les fournisseurs, il écrit les propriétés de configuration dans le profil en appelant [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le nom de la **fonction WIZARDENTRY** doit être placé dans l’entrée WIZARD_ENTRY_NAME dans MAPISVC.INF. 
  
Le nom de la ressource est celui de la ressource de boîte de dialogue qui sera rendue dans le volet de l’Assistant Profil. La ressource qui est passée en arrière doit contenir toutes les pages dans une seule ressource de boîte de dialogue. Lorsque l’Assistant Profil reçoit cette ressource, il ignore le style de la boîte de dialogue, mais pas les styles de contrôle, et crée tous les contrôles en tant qu’enfants de la page Assistant Profil. Tous les contrôles sont initialement masqués. Les fournisseurs doivent s’assurer que les coordonnées de leurs contrôles sont de base zéro ou zéro, et qu’ils ne dépassent pas une largeur maximale de 200 unités de boîte de dialogue et une hauteur maximale de 150 unités de boîte de dialogue. Les identificateurs de contrôle inférieurs à 400 sont réservés à l’Assistant Profil. L’Assistant Profil affiche le titre du fournisseur en gras au-dessus de l’interface utilisateur du fournisseur. 
  
Le pointeur d’interface de propriétés fourni dans le paramètre _lpMAPIProp_ doit être conservé par le fournisseur pour référence ultérieure. L’Assistant Profil traite uniquement de l’ensemble de propriétés le plus élémentaire, et le fournisseur peut utiliser l’implémentation de l’interface de propriétés pour inclure des propriétés supplémentaires. Pendant la configuration, les fournisseurs doivent ajouter leurs propriétés de configuration à l’objet qui implémente l’interface de propriétés. Une fois tous les fournisseurs configurés, l’Assistant Profil ajoute ces propriétés au profil. 
  
Pour plus d’informations sur l’utilisation de cette fonction, voir [Supporting Message Service Configuration](supporting-message-service-configuration.md). 
  

