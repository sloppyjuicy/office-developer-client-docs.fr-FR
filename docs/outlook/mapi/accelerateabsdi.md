---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420373"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel pour traiter les touches d’accès rapide dans une boîte de dialogue de carnet d’adresses sans mode. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction définie implémentée par :  <br/> |MAPI  <br/> |
|Fonction définie appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction. Dans les applications en cours d’exécution sur Microsoft Windows, _ulUIParam_ est le handle de fenêtre parent d’une boîte de dialogue et est de type HWND, cast vers un **ULONG_PTR**. La valeur zéro indique qu’il n’y a pas de fenêtre parente. 
    
 _lpvmsg_
  
> [in] Pointeur vers un Windows message.
    
## <a name="return-value"></a>Valeur renvoyée

Une fonction avec le prototype **ACCELERATEABSDI renvoie** true si elle gère le message. 
  
## <a name="remarks"></a>Remarques

Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue sans mode, c’est-à-dire, uniquement si l’application cliente a définie l’indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM.](adrparm.md) 
  
Une boîte de dialogue sans mode partage la boucle de messages Windows de l’application cliente, au lieu d’avoir sa propre boucle. L’application, qui contrôle la boucle de messages, ne sait pas quelles touches d’accès rapide la boîte de dialogue utilise. Elle appelle donc une fonction **ACCELERATEABSDI** pour tester et agir sur des touches d’accès rapide telles que Ctrl+P pour l’impression. 
  
La boucle de messages d’un client appelle la fonction **ACCELERATEABSDI** lorsque le client appelle une boîte de dialogue de carnet d’adresses sans mode avec la méthode [IAddrBook::Address.](iaddrbook-address.md) Cet appel est interrompu lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS.](dismissmodeless.md) 
  

