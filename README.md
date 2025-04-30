import java.io.FileWriter;
import java.io.IOException;

public class ReadmeGenerator {
    public static void main(String[] args) {
        String content = """
                # JankenGame

                ## 概要
                JankenGameは、シンプルなじゃんけんゲームを実装したプロジェクトです。このリポジトリは、Javaを使用して開発されています。

                ## 特徴
                - プレイヤーとコンピュータが対戦するじゃんけんゲーム
                - 勝敗のロジックをシンプルかつ明確に実装
                - 学習目的で簡単にカスタマイズ可能

                ## 使用方法
                1. このリポジトリをクローンします。
                   ```bash
                   git clone https://github.com/ibuki-hanada/JankenGame.git
                   ```
                2. プロジェクトをお使いのJava IDEで開きます。
                3. メインファイルを実行してゲームをプレイします。

                ## 必要条件
                - Java Development Kit (JDK) 11以上

                ## ファイル構成
                - **Main.java**: ゲームのエントリーポイント
                - **GameLogic.java**: じゃんけんのロジックを含む
                - **README.md**: このプロジェクトの説明

                ## 貢献
                プロジェクトへの貢献を歓迎します！バグの報告、機能の提案、プルリクエストをお待ちしています。

                ## ライセンス
                このプロジェクトはMITライセンスのもとで提供されています。詳細については[LICENSE](LICENSE)ファイルをご覧ください。
                """;

        try (FileWriter writer = new FileWriter("README.md")) {
            writer.write(content);
            System.out.println("README.md ファイルが作成されました！");
        } catch (IOException e) {
            System.err.println("README.md の作成中にエラーが発生しました: " + e.getMessage());
        }
    }
}
