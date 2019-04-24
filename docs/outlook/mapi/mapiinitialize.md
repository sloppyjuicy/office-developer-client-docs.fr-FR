---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346640"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Incrémente le nombre de références du sous-système MAPI et initialise les données globales pour la DLL MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Paramètres

 _lpMapiInit_
  
> dans Pointeur vers une structure [MAPIINIT_0](mapiinit_0.md) . Le paramètre _lpMapiInit_ peut être défini sur null. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le sous-système MAPI a été correctement initialisé.
    
## <a name="remarks"></a>Remarques

La fonction **MAPIInitialize** incrémente le nombre de références MAPI pour le sous-système MAPI et la fonction [MAPIUninitialize](mapiuninitialize.md) décrémente le nombre de références internes. Par conséquent, le nombre d'appels à une fonction doit être égal au nombre d'appels à l'autre. **MAPIInitialize** renvoie S_OK si MAPI n'a pas été précédemment initialisé. 
  
Un client ou un fournisseur de services doit appeler **MAPIInitialize** avant d'établir tout autre appel MAPI. Si ce n'est pas le cas, les appels du client ou du fournisseur de services renvoient la valeur MAPI_E_NOT_INITIALIZED. 
  
Lors de l'appel de **MAPIInitialize** à partir d'une application multithread, définissez le paramètre _lpMapiInit_ sur une structure [MAPIINIT_0](mapiinit_0.md) qui est déclarée comme suit: 
  
 **MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
et appelez: 
  
 **MAPIInitialize** (&amp;MAPIINIT); 
  
Lorsque cette structure est déclarée, MAPI crée un thread distinct pour gérer la fenêtre de notification, qui continue jusqu'à ce que le nombre de références d'initialisation tombe à zéro. Un service Windows doit définir le membre **ulflags** de la structure **MAPIINIT_0** vers laquelle pointe _lpMapiInit_ vers MAPI_NT_SERVICE. 
  
> [!NOTE]
> Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d'une fonction **DllMain** Win32 ou de toute autre fonction qui crée ou termine des threads. Pour plus d'informations, consultez la rubrique [utilisation d'objets thread-safe](using-thread-safe-objects.md). 
  
 **MAPIInitialize** ne renvoie aucune information d'erreur étendue. Contrairement à la plupart des autres appels MAPI, la signification de ses valeurs de retour est strictement définie pour correspondre à l'étape particulière de l'initialisation qui a échoué: 
  
1. Vérifie les paramètres et les indicateurs.
    
    MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS. L'appelant a passé un paramètre ou un indicateur non valide.
    
2. Initialise les clés de Registre requises par MAPI et confirme le type de système d'exploitation. Cette étape se produit uniquement si le processus client est exécuté en tant que service sous Windows et définit l'indicateur de SERVICE MAPI_NT dans la structure **MAPIINIT_0** . 
    
    MAPI_E_TOO_COMPLEX. Le processus appelant est un service Windows et les clés de Registre requises par MAPI n'ont pas pu être initialisées. 
    
    Des informations supplémentaires peuvent être disponibles dans le journal des événements d'application.
    
3. Vérifiez la compatibilité de MAPI avec OLE, puis initialisez OLE.
    
1. Vérifie la compatibilité entre les versions actuelles d'OLE et MAPI. 
    
    MAPI_E_VERSION. La version d'OLE installée sur la station de travail n'est pas compatible avec cette version de MAPI.
    
2. Initialise OLE. 
    
    Au cours de cette étape uniquement, cette fonction peut renvoyer un code d'erreur non répertorié ici. Toute erreur _non_ répertoriée ici doit être supposée provenir de la **CoInitialize**de la fonction OLE.
    
4. Initialise les variables globales par processus.
    
    MAPI_E_SESSION_LIMIT. MAPI définit le contexte spécifique au processus actuel. Des échecs peuvent se produire sur Win16 si le nombre de processus dépasse un certain nombre ou sur n'importe quel système si la mémoire disponible est épuisée.
    
5. Initialise les variables globales partagées de tous les processus.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Les ressources système disponibles sont insuffisantes pour terminer l'opération.
    
6. Initialise le moteur de notification, crée sa fenêtre et son thread s'il est demandé par l'indicateur MAPI_MULTITHREAD_NOTIFICATIONS. 
    
    MAPI_E_INVALID_OBJECT. Peut échouer si les ressources système sont épuisées. 
    
7. Charge et initialise le fournisseur de profils. Vérifie que **MAPIInitialize** peut accéder à la clé de registre où sont stockées les données de profil. 
    
    MAPI_E_NOT_INITIALIZED. Le fournisseur de profils a rencontré une erreur. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> ||MFCMAPI utilise la méthode **MAPIInitialize** pour initialiser MAPI sur un thread d'arrière-plan pour effectuer un traitement de table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

