# Jpin

# monitoring system

This is an example of a class diagram using Mermaid in GitHub.

```mermaid

graph TD
    A[プログラムの開始] --> B[通知リストを作成]
    B --> C[センサーを初期化]
    C --> D[センサーの状態を使用中に設定]
    D --> E{notifyStatusを呼び出す}
    E --> F[メッセージを'Occupied'に設定]
    F --> G[現在の日時でNotificationオブジェクトを作成]
    G --> H[通知を通知リストに追加]
    H --> I[センサーの状態を空きに設定]
    I --> J{notifyStatusを呼び出す}
    J --> K[メッセージを'Vacant'に設定]
    K --> L[現在の日時でNotificationオブジェクトを作成]
    L --> M[通知を通知リストに追加]
    M --> N[通知リストの通知をすべて表示]
    N --> O[プログラムの終了]

    subgraph センサー初期化
        C --> C1[センサー識別IDを設定]
        C1 --> C2[センサー設置場所を設定]
        C2 --> C3[通知リストを設定]
    end

    subgraph notifyStatus
        E --> E1[センサーの状態をチェック]
        E1 --> E2{センサーが使用中か?}
        E2 -->|Yes| F
        E2 -->|No| K
    end



