---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a5331fbb534b3d0b9d9a4010ed753f68357126db
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632531"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Incrémente le nombre de références du sous-système MAPI et initialise les données globales pour la DLL MAPI. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Paramètres

 _lpMapiInit_
  
> [in] Pointeur vers une [structure MAPIINIT_0](mapiinit_0.md) de base. Le  _paramètre lpMapiInit_ peut être définie sur NULL. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le sous-système MAPI a été initialisé avec succès.
    
## <a name="remarks"></a>Remarques

La **fonction MAPIInitialize** incrémente le nombre de références MAPI pour le sous-système MAPI, et la fonction [MAPIUninitialize](mapiuninitialize.md) décrémente le nombre de références internes. Par conséquent, le nombre d’appels à une fonction doit être égal au nombre d’appels à l’autre. **MAPIInitialize** renvoie S_OK si MAPI n’a pas été initialisé précédemment. 
  
Un client ou un fournisseur de services doit appeler **MAPIInitialize** avant d’effectuer tout autre appel MAPI. Si vous ne le faites pas, les appels du client ou du fournisseur de services retournent la MAPI_E_NOT_INITIALIZED valeur. 
  
Lorsque vous appelez **MAPIInitialize** à partir d’une application multithread, définissez le paramètre  _lpMapiInit_ sur une structure [MAPIINIT_0](mapiinit_0.md) déclarée comme suit : 
  
 **MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
et appelez : 
  
 **MAPIInitialize** (&amp;MAPIINIT) ; 
  
Lorsque cette structure est déclarée, MAPI crée un thread distinct pour gérer la fenêtre de notification, qui se poursuit jusqu’à ce que le nombre de références d’initialisation tombe à zéro. Un service Windows doit définir le membre **lags** de la structure **MAPIINIT_0** pointée par _lpMapiInit_ sur MAPI_NT_SERVICE. 
  
> [!NOTE]
> Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d’une fonction **Win32 DllMain** ou toute autre fonction qui crée ou termine des threads. Pour plus d’informations, [voir Using Thread-Safe Objects](using-thread-safe-objects.md). 
  
 **MAPIInitialize ne** retourne aucune information d’erreur étendue. Contrairement à la plupart des autres appels MAPI, les significations de ses valeurs de retour sont strictement définies pour correspondre à l’étape particulière de l’initialisation qui a échoué : 
  
1. Vérifie les paramètres et les indicateurs.
    
    MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS. L’appelant a transmis un paramètre ou un indicateur non valide.
    
2. Initialise les clés de Registre requises par MAPI et confirme le type de système d’exploitation. Cette étape se produit uniquement si le processus client s’exécute en tant que service sous Windows et définit l’indicateur MAPI_NT SERVICE dans la structure **MAPIINIT_0**. 
    
    MAPI_E_TOO_COMPLEX. Le processus appelant est un service Windows et les clés de Registre requises par MAPI n’ont pas pu être initialisées. 
    
    Des informations supplémentaires peuvent être disponibles dans le journal des événements de l’application.
    
3. Vérifiez la compatibilité de MAPI avec OLE, puis initialisez OLE.
    
1. Vérifie la compatibilité entre les versions actuelles de OLE et MAPI. 
    
    MAPI_E_VERSION. La version de OLE installée sur la station de travail n’est pas compatible avec cette version de MAPI.
    
2. Initialise OLE. 
    
    Au cours de cette étape uniquement, cette fonction peut renvoyer un code d’erreur non répertorié ici. Toute erreur  _non_ répertoriée ici doit être supposée être provenant de la fonction OLE **CoInitialize**.
    
4. Initialise les variables globales par processus.
    
    MAPI_E_SESSION_LIMIT. MAPI définit un contexte spécifique au processus actuel. Des défaillances peuvent se produire sur Win16 si le nombre de processus dépasse un certain nombre, ou sur un système si la mémoire disponible est épuisée.
    
5. Initialise les variables globales partagées de tous les processus.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Il n’y avait pas assez de ressources système disponibles pour terminer l’opération.
    
6. Initialise le moteur de notification, crée sa fenêtre et son thread si l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS le demande. 
    
    MAPI_E_INVALID_OBJECT. Peut échouer si les ressources système sont épuisées. 
    
7. Charge et initialise le fournisseur de profils. Vérifie que **MAPIInitialize** peut accéder à la clé de Registre dans laquelle les données de profil sont stockées. 
    
    MAPI_E_NOT_INITIALIZED. Le fournisseur de profils a rencontré une erreur. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI utilise la **méthode MAPIInitialize** pour initialiser MAPI sur un thread d’arrière-plan pour traiter certaines tables. |
   
## <a name="see-also"></a>Consultez aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

