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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356412"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel appelée par l'Assistant Profil pour permettre à un fournisseur de services de réagir aux événements de l'utilisateur lorsque les pages ou les feuilles de propriétés du fournisseur sont affichées. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz. h  <br/> |
|Fonction définie implémentée par:  <br/> |Fournisseurs de services  <br/> |
|Fonction définie appelée par:  <br/> |Assistant Profil MAPI  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

_hDlg_
  
> dans Handle de fenêtre dans la boîte de dialogue Assistant Profil. 
    
_wMsgID_
  
> dans Message de fenêtre à traiter. Outre les messages de fenêtre standard attendus par une boîte de dialogue modale, les messages suivants peuvent être reçus:
    
WM_CLOSE 
  
> L'Assistant Profil est terminé. Le fournisseur de services doit effectuer tout le nettoyage requis, par exemple en désallouant toute mémoire allouée dynamiquement. 
    
WM_COMMAND 
  
> L'un des contrôles du fournisseur a été sélectionné ou l'utilisateur a cliqué sur le bouton **suivant** ou **précédent** . La valeur dans le paramètre _wParam_ indique quels événements utilisateur ont eu lieu. 
    
WM_INITDIALOG 
  
> L'utilisateur a été déplacé vers une autre page de propriétés, pour laquelle la boîte de dialogue doit être initialisée. Le fournisseur doit initialiser les contrôles que l'Assistant Profil a ajoutés à la boîte de dialogue. 
    
WIZ_QUERYNUMPAGES 
  
> L'Assistant Profil demande le nombre de pages que le fournisseur doit afficher. Le fournisseur doit renvoyer le nombre de pages au lieu de TRUE ou FALSe. Par exemple, utilisez l'instruction return suivante pour indiquer que trois pages doivent être affichées:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> dans Paramètre 32 bits associé aux messages de fenêtre. Les valeurs possibles dépendent du message spécifié dans le paramètre _wMsgID_ . En plus des valeurs attendues avec les messages de fenêtre standard pour une boîte de dialogue modale, les valeurs suivantes peuvent être reçues: 
    
WIZ_NEXT 
  
> Lorsque _wMsgID_ contient WM_COMMAND, l'utilisateur a cliqué sur le bouton **suivant** . 
    
WIZ_PREV 
  
> Lorsque _wMsgID_ contient WM_COMMAND, l'utilisateur a cliqué sur le bouton **précédent** . 
    
_lParam_
  
> dans Paramètre 32 bits associé aux messages de fenêtre. Les valeurs possibles dépendent du message spécifié dans le paramètre _wMsgID_ . 
    
## <a name="return-value"></a>Valeur renvoyée

La valeur renvoyée par une fonction basée sur **SERVICEWIZARDDLGPROC** dépend du message de fenêtre reçu. Notez en particulier la valeur de retour exceptionnelle pour le message WIZ_QUERYNUMPAGES. Les valeurs de retour normales sont les suivantes: 
  
TRUE 
  
> Le fournisseur de services a traité le message de fenêtre received. 
    
FALSE 
  
> Le fournisseur de services n'a pas traité le message de fenêtre received.
    
## <a name="remarks"></a>Remarques

Lorsque l'utilisateur passe d'une page de propriétés à une autre, le fournisseur est chargé de masquer les contrôles de l'ancienne page et d'afficher les contrôles de la page suivante ou précédente. Lorsque l'utilisateur clique sur le bouton **suivant** , la fonction basée sur **SERVICEWIZARDDLGPROC** est appelée avec le message WM_COMMAND et WIZ_NEXT dans le paramètre _wParam_ . Les étapes suivantes décrivent ce qui se passe entre le moment où l'utilisateur clique sur **suivant** et l'heure à laquelle les pages de configuration du premier fournisseur sont affichées. 
  
1. L'Assistant Profil masque tous les contrôles de la fenêtre. 
    
2. L'Assistant Profil ajoute les contrôles masqués du fournisseur à la page. 
    
3. L'Assistant Profil appelle **SERVICEWIZARDDLGPROC**, en envoyant le message WM_INITDIALOG, afin que le fournisseur puisse initialiser les contrôles. 
    
4. L'Assistant Profil appelle **SERVICEWIZARDDLGPROC**, en envoyant le message WIZ_QUERYNUMPAGES. Le fournisseur renvoie le nombre de pages à afficher. 
    
5. L'Assistant Profil appelle **SERVICEWIZARDDLGPROC**, en envoyant le message WM_COMMAND avec le paramètre _wParam_ défini sur WIZ_NEXT ou WIZ_PREV. À ce stade, le fournisseur renvoie la valeur FALSe {erreur} ou révèle ses contrôles et renvoie la valeur TRUE {Success}. Si l'Assistant Profil passe dans ID_NEXT, la première page du fournisseur s'affiche. Si ID_PREV est transmis, la dernière page est affichée. 
    
6. L'Assistant Profil appelle la fonction **SERVICEWIZARDDLGPROC** du fournisseur, en envoyant le message WM_COMMAND avec le paramètre _wParam_ défini sur WIZ_NEXT ou WIZ_PREV (selon le bouton sur lequel l'utilisateur a cliqué). Le fournisseur est responsable de l'affichage ou du masquage de ses contrôles et de l'écriture de ses données dans le **IMAPIProp** transmis à l'Assistant Profil pour parcourir sa séquence de pages. Le fournisseur doit renvoyer la valeur TRUE si la page suivante ou précédente a été correctement affichée, et la valeur FALSe si ni la page suivante ni la page précédente ne peuvent être affichées. Le fournisseur doit être conscient lorsqu'il est pas à l'extérieur de sa séquence de pages et répond de manière appropriée en masquant ses contrôles et en écrivant ses données dans le profil. 
    
7. Si l'utilisateur se trouve à l'extérieur de la plage de pages du fournisseur, l'Assistant Profil supprime les contrôles masqués du fournisseur dans la boîte de dialogue et appelle le fournisseur suivant ou affiche sa page suivante s'il s'agissait du dernier fournisseur. 
    

