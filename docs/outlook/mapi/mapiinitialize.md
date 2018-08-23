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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5fcebd1fefa0d077acbe62a45a19a622e13b35fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587368"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Incrémente le décompte de références du sous-système MAPI et initialise les données globales de la DLL MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Paramètres

 _lpMapiInit_
  
> [in] Pointeur vers une structure [MAPIINIT_0](mapiinit_0.md) . Le paramètre _lpMapiInit_ peut être défini sur NULL. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le sous-système MAPI a été correctement initialisé.
    
## <a name="remarks"></a>Remarques

Les incréments de fonction **exécuter MAPIInitialize** le MAPI décompte de références pour le sous-système MAPI et la décrémente de fonction [MAPIUninitialize](mapiuninitialize.md) l’interne décompte de références. Par conséquent, le nombre d’appels à une fonction doit correspondre au nombre d’appels à l’autre. **Exécuter MAPIInitialize** renvoie S_OK si MAPI n’a pas déjà été initialisé. 
  
Un client ou fournisseur de services doit appeler **exécuter MAPIInitialize** avant d’effectuer n’importe quel autre appel MAPI. Cela entraîne client ou le service fournisseur appelle renvoyer la valeur MAPI_E_NOT_INITIALIZED. 
  
Lorsque vous appelez **exécuter MAPIInitialize** à partir d’une application multithread, définissez le paramètre _lpMapiInit_ vers une structure [MAPIINIT_0](mapiinit_0.md) qui est déclarée comme suit : 
  
 **MAPIINIT_0** MAPIINIT = {0 MAPI_MULTITHREAD_NOTIFICATIONS} 
  
et l’appel : 
  
 **Exécuter MAPIInitialize** (&amp;MAPIINIT) ; 
  
Lorsque cette structure est déclarée, MAPI crée un thread distinct pour gérer la fenêtre de notification, qui se poursuit jusqu'à ce que le décompte de références initialize descend à zéro. Un service Windows doit définir le membre **ulflags** de la structure **MAPIINIT_0** désigné par _lpMapiInit_ à MAPI_NT_SERVICE. 
  
> [!NOTE]
> Impossible d’appeler **exécuter MAPIInitialize** ou **MAPIUninitialize** au sein d’une fonction Win32 **DllMain** ou toute autre fonction qui crée ou met fin à des threads. Pour plus d’informations, voir [Utilisation des objets Thread-Safe](using-thread-safe-objects.md). 
  
 **Exécuter MAPIInitialize** ne renvoie pas les informations d’erreur étendue. Contrairement à la plupart des appels MAPI, la signification de ses valeurs de retour est définie strictement pour correspondre à l’étape particulière de l’initialisation a échoué : 
  
1. Vérifie les paramètres et les indicateurs.
    
    MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS. Appelant transmis indicateur ou paramètre non valide.
    
2. Initialise les clés de Registre requises par MAPI et confirme le type du système d’exploitation. Cette étape se produit uniquement si le processus de client s’exécute en tant que service sous Windows et définit l’indicateur de SERVICE MAPI_NT dans la structure **MAPIINIT_0** . 
    
    MAPI_E_TOO_COMPLEX. Le processus appelant est un service Windows et clés de Registre requises par MAPI n’a pas peuvent être initialisés. 
    
    Des informations supplémentaires peuvent être disponibles dans le journal des événements.
    
3. Vérifier la compatibilité de MAPI avec OLE, puis initialiser OLE.
    
1. Vérifie la compatibilité entre les versions actuelles de OLE et MAPI. 
    
    MAPI_E_VERSION. La version de OLE installée sur la station de travail n’est pas compatible avec cette version de MAPI.
    
2. Initialise OLE. 
    
    Au cours de cette étape uniquement, cette fonction peut renvoyer un code d’erreur non répertorié ici. Toute erreur _non_ répertoriés ici doit être supposé provenant de la fonction OLE **CoInitialize**.
    
4. Initialise les variables globales par processus
    
    MAPI_E_SESSION_LIMIT. MAPI définit les cadre spécifique dans le processus en cours. Échecs peuvent se produire si le nombre de processus dépasse un certain nombre de Win16, ou sur n’importe quel système si la mémoire disponible est saturée.
    
5. Initialise partagées des variables globales de tous les processus.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Pas de suffisamment de ressources système était disponibles pour terminer l’opération.
    
6. Initialise le moteur de notification, crée une fenêtre et son thread si demandée par l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS. 
    
    MAPI_E_INVALID_OBJECT. Peut échouer si épuisement des ressources système. 
    
7. Charge et initialise le fournisseur de profils. Vérifie que **exécuter MAPIInitialize** peut accéder à la clé de Registre où sont stockées les données de profil. 
    
    MAPI_E_NOT_INITIALIZED. Le fournisseur de profils a rencontré une erreur. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI utilise la méthode **exécuter MAPIInitialize** pour initialiser MAPI sur une thread d’arrière-plan pour effectuer un traitement du tableau.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

