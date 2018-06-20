---
title: Propriété Cannonical PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 62bc0e75d0a405ebe9f68ec9f4af1ca038bda219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786023"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propriété Cannonical PidTagFolderWebViewInfo

  
  
**S’applique à**: Outlook 
  
Contient l’URL de la page d’accueil d’un dossier dans Microsoft Outlook. Cette propriété contient un flux binaire appelé **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificateur :  <br/> |0x36DF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Dossier MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Une URL de page d’accueil peut être spécifiée pour n’importe quel dossier Outlook. Ces informations sont accessibles dans Outlook à partir de l’onglet de la **Page d’accueil** de la boîte de dialogue Propriétés d’un dossier. 
  
En fonction de certains paramètres de stratégie, la page d’accueil peut être ignorée par Outlook si la banque MAPI qui contient ce dossier ne signale pas MSCAP_SECURE_FOLDER_HOMEPAGES dans son implémentation [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) . 
  
Le dossier **Outlook aujourd'hui** et un dossier public peuvent avoir des URL de page d’accueil. Toutefois le dossier **Outlook aujourd'hui** utilise un autre mécanisme pour gérer les URL de sa page d’accueil ; Ce mécanisme n’est pas couvertes dans cette rubrique. Un dossier public peut également avoir une URL de page d’accueil définie dans ce qui est spécifique à un utilisateur. Toutefois, cette fonctionnalité n’est pas décrite dans cette rubrique. 
  
La valeur de cette propriété est un flux binaire appelé **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Structure de flux WebViewPersistenceObject

La structure de flux **WebViewPersistenceObject** contient des informations sur une URL de page d’accueil d’un dossier. 
  
Éléments de données dans cette structure sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre suivant spécifié. 
  
> [!NOTE]
> La description suivante peut ne pas contenir toutes les valeurs de champ pris en charge par Outlook. Par conséquent, lorsque votre code lit un flux existant, des indicateurs qui ne sont pas répertoriés ici peuvent également se trouver. Toutefois, vous pouvez utiliser cette description pour créer par programme des valeurs de la propriété **PidTagFolderWebViewInfo** maîtriser Outlook. 
  
 _dwVersion_
  
> Valeur DWORD (4 octets). La version du format de la structure. Microsoft Office Outlook 2007, la seule valeur pris en charge pour ce champ est comme suit.
    
|**Nom de valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> Valeur DWORD (4 octets). Le type d’informations de la page d’accueil. Microsoft Office Outlook 2007, la seule valeur pris en charge pour ce champ est comme suit.
    
|**Nom de valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> Valeur DWORD (4 octets). Une combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant.
    
|Indicateur nom ***|****Valeur****|****Description****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |La case à cocher **Afficher la page d’accueil par défaut pour ce dossier** a été activée dans l’onglet **Page d’accueil** de la boîte de dialogue Propriétés d’un dossier.  <br/> |
   
 _dwUnused [7]_
  
> Tableau 7 éléments DWORD (nombre total de 28 octets). Non utilisé.
    
cbData
  
> ULONG (4 octets). La taille, en octets, de l’élément de données _wzURL_ . 
    
 _wzURL_
  
> Tableau d’éléments WCHAR. La représentation UTF-16 de la chaîne d’URL de page d’accueil se terminant par zéro.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Exemple de flux de données WebViewPersistenceObject

Cette section décrit un exemple d’un flux **WebViewPersistenceObject** . Le flux Spécifie l’URL de la page d’accueil «http://www.microsoft.com». 
  
 **Vidage des données**
  
Vous trouverez ci-dessous un vidage des données de l’objet stream tel qu’il doit être affiché dans un éditeur binaire.
  
|**Décalage de flux**|**Octets de données**|**Données ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Vous trouverez ci-dessous une analyse des données pour le flux **WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Décalage de 0 x 0, 4 octets : 0 x 00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Décalage de 0 x 4, 4 octets : 0 x 00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Décalage de 0 x 8, 4 octets : 0 x 00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused [7]_
  
> Décalage 0xC, 28 octets : tous les zéros.
    
 _cbData_
  
> Décalage de 0 x 28, 4 octets : 0 x 00000032.
    
 _wzURL_
  
> Décalage 0x2C, 0 x 32 octets : tableau de 25 WCHAR. Une valeur de chaîne terminée par zéro Unicode : «http://www.microsoft.com».
    

