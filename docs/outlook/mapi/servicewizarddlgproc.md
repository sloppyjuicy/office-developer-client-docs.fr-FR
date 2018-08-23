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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fdd5d01b96c9ea756ee64f113ccb5119a9693668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594466"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel appelée par l’Assistant profil pour autoriser un fournisseur de services de réagir aux événements utilisateur lorsque les feuilles de propriétés ou des pages du fournisseur sont affichés. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz.h  <br/> |
|Fonction implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |Assistant profil MAPI  <br/> |
   
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
  
> [in] Handle de fenêtre pour la boîte de dialogue Assistant profil. 
    
_wMsgID_
  
> [in] Le message de fenêtre à traiter. Outre les messages de fenêtre normale attendus par une boîte de dialogue modale, les messages suivants peuvent être reçus :
    
WM_CLOSE 
  
> L’Assistant profil est terminée. Le fournisseur de services doit faire tout le nettoyage requis tels que les libérer dynamiquement de mémoire allouée. 
    
WM_COMMAND 
  
> Un des contrôles du fournisseur a été sélectionné, ou le bouton **suivant** ou **précédent** a été utilisé. La valeur du paramètre _wParam_ indique lequel de ces événements utilisateur s’est produite. 
    
WM_INITDIALOG 
  
> L’utilisateur a déplacé vers une autre page de propriétés, dont la boîte de dialogue doit être initialisée. Le fournisseur doit initialiser les contrôles de l’Assistant profil a ajouté à la boîte de dialogue. 
    
WIZ_QUERYNUMPAGES 
  
> L’Assistant profil demande le nombre de pages que le fournisseur doit afficher. Le fournisseur doit renvoyer le nombre de pages au lieu de la valeur TRUE ou FALSE. Par exemple, utilisez l’instruction suivante de retour pour indiquer que trois pages doivent être affichée :
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Un paramètre de 32 bits associé à des messages de fenêtre. Le message spécifié dans le paramètre _wMsgID_ dépendent de valeurs possibles. Outre les valeurs prévus avec les messages de fenêtre normale pour une boîte de dialogue modale, les valeurs suivantes peuvent être reçus : 
    
WIZ_NEXT 
  
> Lorsque _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur le bouton **suivant** . 
    
WIZ_PREV 
  
> Lorsque _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur le bouton **précédent** . 
    
_lParam_
  
> [in] Un paramètre de 32 bits associé à des messages de fenêtre. Le message spécifié dans le paramètre _wMsgID_ dépendent de valeurs possibles. 
    
## <a name="return-value"></a>Valeur renvoy�e

La valeur renvoyée par une fonction **SERVICEWIZARDDLGPROC** en fonction de dépend de la fenêtre message reçu. Notez en particulier que les exceptionnelles renvoient la valeur pour le message WIZ_QUERYNUMPAGES. Les valeurs de retour normales sont : 
  
TRUE 
  
> Le fournisseur de services a traité le message reçu. 
    
FALSE 
  
> Le fournisseur de services n’a pas traité le message reçu.
    
## <a name="remarks"></a>Remarques

Lorsque l’utilisateur passe d’une page de propriété à une autre, le fournisseur est chargé de masquer les contrôles de la page ancienne et affiche les contrôles de la page suivante ou précédente. Lorsque l’utilisateur clique sur le bouton **suivant** , la fonction **SERVICEWIZARDDLGPROC** en fonction est appelée avec le message WM_COMMAND et WIZ_NEXT dans le paramètre _wParam_ . Les étapes suivantes décrivent ce qui se produit entre le temps que l’utilisateur clique sur **suivant** et lors du rendu des pages de configuration du premier fournisseur. 
  
1. L’Assistant profil masquer tous les contrôles qui se trouvent dans la fenêtre. 
    
2. L’Assistant profil ajoute les contrôles masqués du fournisseur à la page. 
    
3. L’Assistant profil appelle **SERVICEWIZARDDLGPROC**, envoyer le message WM_INITDIALOG, afin que le fournisseur peut initialiser les contrôles. 
    
4. L’Assistant profil appelle **SERVICEWIZARDDLGPROC**, l’envoi du message WIZ_QUERYNUMPAGES. Le fournisseur renvoie le nombre de pages à afficher. 
    
5. L’Assistant profil appelle **SERVICEWIZARDDLGPROC**, envoyer le message WM_COMMAND avec le paramètre _wParam_ défini sur WIZ_NEXT ou WIZ_PREV. À ce stade, le fournisseur soit renvoie la valeur FALSE {erreur} ou révèle ses contrôles et renvoie la valeur TRUE {réussite}. Si l’Assistant profil passe ID_NEXT, la première page du fournisseur s’affiche. Si ID_PREV est passé, la dernière page s’affiche. 
    
6. L’Assistant profil appelle fonction **SERVICEWIZARDDLGPROC** du fournisseur d’envoyer le message WM_COMMAND avec le paramètre _wParam_ défini sur WIZ_NEXT ou WIZ_PREV (selon le bouton sur lequel l’utilisateur a cliqué). Le fournisseur est responsable de l’affichage ou masquage de ses contrôles et écriture de ses données dans **IMAPIProp** passé à l’Assistant profil afin de parcourir la séquence de pages. Le fournisseur doit retourner la valeur TRUE si la page suivante ou précédente a été correctement affichée, et FALSE si ni la page suivante ou précédente peut être affichée. Le fournisseur doit tenir compte lorsqu’il est pas en dehors de la séquence de pages et répondre de façon appropriée en masquant ses contrôles et en écriture de ses données dans le profil. 
    
7. Si les étapes de l’utilisateur en dehors de la plage du fournisseur de pages, l’Assistant profil supprime les contrôles masqués du fournisseur de la boîte de dialogue et appelle le fournisseur suivant ou affiche la page suivante, si c’était le dernier fournisseur. 
    

