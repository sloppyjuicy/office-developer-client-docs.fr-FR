---
title: Propriété canonique PidTagFolderWebViewInfo
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
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316309"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propriété canonique PidTagFolderWebViewInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'URL de la page d'accueil d'un dossier dans Microsoft Outlook. Cette propriété contient un flux binaire appelé **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificateur :  <br/> |0x36DF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Dossier MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Une URL de page d'accueil peut être spécifiée pour n'importe quel dossier Outlook. Ces informations sont accessibles dans Outlook à partir de l'onglet **page d'accueil** de la boîte de dialogue Propriétés d'un dossier. 
  
En fonction de certains paramètres de stratégie, la page d'accueil peut être ignorée par Outlook si le magasin MAPI qui contient ce dossier ne rapporte pas MSCAP_SECURE_FOLDER_HOMEPAGES dans son implémentation [IMSCapabilities:: GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) . 
  
Le dossier **Outlook aujourd'hui** et un dossier public peuvent avoir des URL de page d'accueil. Toutefois, le dossier **Outlook aujourd'hui** utilise un autre mécanisme pour gérer l'URL de sa page d'accueil; ce mécanisme n'est pas abordé dans cette rubrique. Un dossier public peut également comporter une URL de page d'accueil qui est spécifique à un utilisateur. Toutefois, cette fonctionnalité n'est pas décrite dans cette rubrique. 
  
La valeur de cette propriété est un flux binaire appelé **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Structure de flux WebViewPersistenceObject

La structure de flux **WebViewPersistenceObject** contient des informations sur l'URL d'une page d'accueil pour un dossier. 
  
Les éléments de données dans cette structure sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre spécifié. 
  
> [!NOTE]
> La description suivante peut ne pas répertorier toutes les valeurs de champ prises en charge par Outlook; par conséquent, lorsque votre code lit un flux existant, certains indicateurs qui ne sont pas répertoriés ici peuvent également être trouvés. Toutefois, vous pouvez utiliser cette description pour créer par programme des valeurs pour la propriété **PidTagFolderWebViewInfo** qu'Outlook va comprendre. 
  
 _dwVersion_
  
> DWORD (4 octets). Version du format de la structure. À partir de Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.
    
|**Nom de la valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 octets). Type des informations de la page d'accueil. À partir de Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.
    
|**Nom de la valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 octets). Une combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant.
    
|Nom de l'indicateur * * * *|****Valeur****|****Description****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |La case à cocher **afficher la page d'accueil par défaut pour ce dossier** a été activée dans l'onglet **page d'accueil** de la boîte de dialogue Propriétés d'un dossier.  <br/> |
   
 _dwUnused [7]_
  
> Tableau de 7 éléments DWORD (28 octets au total). Inutilisés.
    
cbData
  
> ULONG (4 octets). Taille, en octets, de l'élément de données _wzURL_ . 
    
 _wzURL_
  
> Tableau d'éléments WCHAR. La représentation UTF-16 de la chaîne d'URL de la page d'accueil se terminant par un zéro.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Exemple de flux WebViewPersistenceObject

Cette section décrit un exemple de flux **WebViewPersistenceObject** . Le flux spécifie l'URL de lahttps://www.microsoft.compage d'accueil «». 
  
 **Vidage des données**
  
Voici un dump des données du flux tel qu'il s'afficherait dans un éditeur binaire.
  
|**Décalage de flux**|**Octets de données**|**Données ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Voici une analyse des exemples de données pour le flux **WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Offset 0x0, 4 octets: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Offset 0x4, 4 octets: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Décalage 0x8, 4 octets: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused [7]_
  
> Offset 0xC, 28 octets: tous les zéros.
    
 _cbData_
  
> Décalage 0x28, 4 octets: 0x00000032.
    
 _wzURL_
  
> Offset 0x2C, 0x32 octets: tableau de 25 WCHARs. Valeur de chaîne se terminant par zéro Unicode:https://www.microsoft.com"".
    

