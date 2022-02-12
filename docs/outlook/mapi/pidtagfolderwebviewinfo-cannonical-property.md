---
title: Propriété canonique PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c30f15c0dc7e5021882628d2f3714357bf4f91df
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773151"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propriété canonique PidTagFolderWebViewInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’URL de la page d’accueil d’un dossier dans Microsoft Outlook. Cette propriété contient un flux binaire appelé **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificateur :  <br/> |0x36DF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Dossier MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Une URL de page d’accueil peut être spécifiée pour tout Outlook dossier. Ces informations sont accessibles dans Outlook à partir de l’onglet **Page** d’accueil de la boîte de dialogue Propriétés d’un dossier. 
  
Selon certains paramètres de stratégie, la page d’accueil peut être ignorée par Outlook si le magasin MAPI qui contient ce dossier ne signale pas MSCAP_SECURE_FOLDER_HOMEPAGES dans son implémentation [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md). 
  
Le dossier **Outlook Aujourd’hui** et un dossier public peuvent avoir des URL de page d’accueil. Toutefois, **le Outlook Today** utilise un mécanisme différent pour gérer l’URL de sa page d’accueil ; ce mécanisme n’est pas abordé dans cette rubrique. Une URL de page d’accueil spécifique à un utilisateur peut également être définie dans un dossier public. Toutefois, cette fonctionnalité n’est pas décrite dans cette rubrique. 
  
La valeur de cette propriété est un flux binaire appelé **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Structure de flux WebViewPersistenceObject

La structure **de flux WebViewPersistenceObject** contient des informations sur une URL de page d’accueil pour un dossier. 
  
Les éléments de données de cette structure sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant. 
  
> [!NOTE]
> La description suivante peut ne pas rés lister toutes les valeurs de champ pris en charge par Outlook ; par conséquent, lorsque votre code lit un flux existant, certains indicateurs qui ne sont pas répertoriés ici peuvent également être trouvés. Toutefois, vous pouvez utiliser cette description pour créer par programme des valeurs pour la propriété **PidTagFolderWebViewInfo** que vous Outlook comprendre. 
  
 _dwVersion_
  
> DWORD (4 octets). Version du format de la structure. Depuis Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.
    
|**Nom de la valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 octets). Type des informations de la page d’accueil. Depuis Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.
    
|**Nom de la valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 octets). Combinaison de zéro ou plus d’indicateurs dont les valeurs et les significations sont répertoriées dans le tableau suivant.
    
|Nom de l’indicateur****|****Valeur****|****Description****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |La **case à** cocher Afficher la page d’accueil par défaut pour ce dossier a été cochée dans l’onglet **Page** d’accueil de la boîte de dialogue Propriétés d’un dossier. |
   
 _dwUnused[7]_
  
> Tableau de 7 éléments DWORD (28 octets au total). Inutilisé.
    
cbData
  
> ULONG (4 octets). Taille, en octets, de l’élément  _de données wzURL_ . 
    
 _wzURL_
  
> Tableau d’éléments WCHAR. Représentation UTF-16 de la chaîne d’URL de page d’accueil sans fin.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Exemple de flux WebViewPersistenceObject

Cette section décrit un exemple de **flux WebViewPersistenceObject** . Le flux spécifie l’URL de la page d’accueil «https://www.microsoft.com ». 
  
 **Vidage de données**
  
Voici un vidage de données du flux tel qu’il serait affiché dans un éditeur binaire.
  
|**Décalage de flux**|**Octets de données**|**Données ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Voici une analyse des exemples de données pour le **flux WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Décalage 0x0, 4 octets : 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Décalage 0x4, 4 octets : 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Décalage 0x8, 4 octets : 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused[7]_
  
> Décalage 0xC, 28 octets : tous les zéros.
    
 _cbData_
  
> Décalage 0x28, 4 octets : 0x00000032.
    
 _wzURL_
  
> Décalage 0x2C, 0x32 octets : tableau de 25 WCHAR. Valeur de chaîne Unicode sans fin : « https://www.microsoft.com ».
    

