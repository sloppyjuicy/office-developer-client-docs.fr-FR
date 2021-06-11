---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432379"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel invoquée par l’Assistant Profil pour permettre à un fournisseur de services de réagir aux événements utilisateur lorsque les pages ou les feuilles de propriétés du fournisseur sont affichées. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz.h  <br/> |
|Fonction définie implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Fonction définie appelée par :  <br/> |Assistant Profil MAPI  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parameters

_hDlg_
  
> [in] Poignée de fenêtre de la boîte de dialogue Assistant Profil. 
    
_wMsgID_
  
> [in] Message de fenêtre à traiter. Outre les messages de fenêtre ordinaire attendus par une boîte de dialogue modale, les messages suivants peuvent être reçus :
    
WM_CLOSE 
  
> L’Assistant Profil est terminé. Le fournisseur de services doit faire tous les nettoyages requis, tels que la désaffectation de toute mémoire allouée dynamiquement. 
    
WM_COMMAND 
  
> L’un des contrôles du fournisseur a  été  sélectionné ou l’utilisateur a cliqué sur le bouton Suivant ou Arrière. La valeur dans le  _paramètre wParam_ indique lequel de ces événements utilisateur s’est produit. 
    
WM_INITDIALOG 
  
> L’utilisateur a été déplacé vers une autre page de propriétés, pour laquelle la boîte de dialogue doit être initialisée. Le fournisseur doit initialiser les contrôles que l’Assistant Profil a ajoutés à la boîte de dialogue. 
    
WIZ_QUERYNUMPAGES 
  
> L’Assistant Profil vous invite à afficher le nombre de pages que le fournisseur doit afficher. Le fournisseur doit renvoyer le nombre de pages au lieu de TRUE ou FALSE. Par exemple, utilisez l’instruction de retour suivante pour indiquer que trois pages doivent être affichées :
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Paramètre 32 bits associé aux messages de fenêtre. Les valeurs possibles dépendent du message spécifié dans le _paramètre wMsgID._ Outre les valeurs attendues avec les messages de fenêtre normal pour une boîte de dialogue modale, les valeurs suivantes peuvent être reçues : 
    
WIZ_NEXT 
  
> Lorsque  _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur **le bouton** Suivant. 
    
WIZ_PREV 
  
> Lorsque  _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur le **bouton** Retour. 
    
_lParam_
  
> [in] Paramètre 32 bits associé aux messages de fenêtre. Les valeurs possibles dépendent du message spécifié dans le _paramètre wMsgID._ 
    
## <a name="return-value"></a>Valeur renvoyée

La valeur renvoyée par une fonction basée sur **SERVICEWIZARDDLGPROC** dépend du message de fenêtre reçu. Notez en particulier la valeur de retour exceptionnelle du message WIZ_QUERYNUMPAGES message. Les valeurs de retour normales sont : 
  
TRUE 
  
> Le fournisseur de services a traitée le message de fenêtre reçue. 
    
FALSE 
  
> Le fournisseur de services n’a pas traitée le message de fenêtre reçue.
    
## <a name="remarks"></a>Remarques

Lorsque l’utilisateur passe d’une page de propriétés à une autre, le fournisseur est chargé de masquer les contrôles de l’ancienne page et d’afficher les contrôles de la page suivante ou précédente. Lorsque l’utilisateur  clique sur le bouton Suivant, la fonction basée sur **SERVICEWIZARDDLGPROC** est appelée avec le message WM_COMMAND et WIZ_NEXT dans le paramètre _wParam._ Les étapes suivantes décrivent ce qui se produit entre le moment où l’utilisateur clique sur **Next** et le moment où les pages de configuration du premier fournisseur sont restituer. 
  
1. L’Assistant Profil masque tous les contrôles de la fenêtre. 
    
2. L’Assistant Profil ajoute les contrôles masqués du fournisseur à la page. 
    
3. L’Assistant Profil appelle **SERVICEWIZARDDLGPROC**, envoyant le message WM_INITDIALOG, afin que le fournisseur puisse initialiser les contrôles. 
    
4. L’Assistant Profil appelle **SERVICEWIZARDDLGPROC**, envoyant le WIZ_QUERYNUMPAGES message. Le fournisseur renvoie le nombre de pages à voir. 
    
5. L’Assistant Profil appelle **SERVICEWIZARDDLGPROC,** envoyant le message WM_COMMAND avec le paramètre  _wParam_ paramétré sur WIZ_NEXT ou WIZ_PREV. À ce stade, le fournisseur renvoie false {error} ou révèle ses contrôles et renvoie TRUE {success}. Si l’Assistant Profil ID_NEXT, la première page du fournisseur s’affiche. Si ID_PREV est transmis, la dernière page s’affiche. 
    
6. L’Assistant Profil appelle la fonction **SERVICEWIZARDDLGPROC** du fournisseur, envoyant le message WM_COMMAND avec le paramètre  _wParam_ paramétré sur WIZ_NEXT ou WIZ_PREV (selon le bouton sur lequel l’utilisateur a cliqué). Le fournisseur est chargé d’afficher ou de masquer ses contrôles et d’écrire ses données dans **l’IMAPIProp** transmis à l’Assistant Profil pour passer pas à pas dans sa séquence de pages. Le fournisseur doit renvoyer TRUE si la page suivante ou précédente a été affichée avec succès, et FALSE si ni la page suivante ni la page précédente ne peuvent être affichées. Le fournisseur doit savoir quand il se trouve en dehors de sa séquence de pages et répondre de manière appropriée en masquant ses contrôles et en écrivant ses données dans le profil. 
    
7. Si l’utilisateur se place en dehors de la plage de pages du fournisseur, l’Assistant Profil supprime les contrôles masqués du fournisseur de la boîte de dialogue et appelle le fournisseur suivant ou affiche sa page suivante s’il s’agit du dernier fournisseur. 
    

